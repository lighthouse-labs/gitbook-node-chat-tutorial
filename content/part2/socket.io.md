# Socket.IO for Real-time messaging

Now it's time to add the last missing, yet crucial piece to our app: _chat functionality_!

To do this, we will leverage yet another 3rd party Node module. It's called Socket.IO.

Check it out here: <http://socket.io/>.

Socket.IO will leverage a technology that browsers have called Web Sockets.

What's nice about Socket.io is that it will let us write similar JS code on both the client (browser) side and at the server (Node) side. 

## Step 1

Run the following command in the terminal window to install it on the server.

``` 
npm install socket.io
```

The output will look something like this.

![Install socket.io](/assets/install-socket.io.png)

## Step 2

Now let's add some code in **server.js** that will use this library. This code block should be placed *before/above* the line of code that starts with `server.listen`.

```javascript
var io = require('socket.io')(server);

io.on('connection', function (socket) {
  socket.on('message', function (msg) {
    io.emit('message', msg);
  });
});
```

## Step 3

Next, we need to add similar logic to the client app.

Open the **index.html** file and modify the `<script>` tags so that we also reference Socket.IO. We can do this by adding one more script tag before our `app.js` script tag, so that it looks like this.

```html
<script src="https://code.jquery.com/jquery-3.1.1.js"></script>
<script src="/socket.io/socket.io.js"></script>
<script src="app.js"></script>
```

## Step 4

Open **app.js**, our client-side JS code file, and let's add some code to send and receive messages from the browser.

Add the following code to the very top of the file.

```javascript
var socket = io();
```

This is saying that `socket` is now a reference to the Socket.IO library.

## Step 5

In that same file, *replace* the line that starts with `alert` line from before with the following code.

```javascript
  socket.emit('message', text);
  $('#message').val('');
```

The code above says to emit the textual message to the server instead of performing our temporary `alert` behaviour. The second line in the code simply clears the input so that another message can be typed by the same user.

We're not done yet, we need to listen for messages that are received from the server and append them into the message list. Add the following code at the *bottom* of the file.

```javascript
socket.on('message', function (msg) {
  $('<li>').text(msg).appendTo('#history');
});
```

This part tells the browser that any time a message is received from the real time web socket connection with the server, create a new `<li>` (list item) HTML element and append it to the message history `<ol>`.

## Final code for app.js

The **app.js** file should look like this.

```javascript
var socket = io();

$('form').submit(function () {
  var text = $('#message').val();
  socket.emit('message', text);
  $('#message').val('');
  return false;
});

socket.on('message', function (msg) {
  $('<li>').text(msg).appendTo('#history');
});
```

## Final code for server.js

The `server.js` file should look like this:

```javascript
var express = require('express');
var app = express();

var http = require('http');
var server = http.Server(app);

app.use(express.static('client'));

var io = require('socket.io')(server);

io.on('connection', function (socket) {
  socket.on('message', function (msg) {
    io.emit('message', msg);
  });
});

server.listen(8080, function() {
  console.log('Chat server running');
});
```

## Whoa, it works!

Make sure all your files are saved, and the Node server is still running, and give it a shot.

That's right, it works! That's all it took. The basic chat functionality works. Have your peer go to the same URL that you're on and you guys should be able to communicate!

Note: newcomers to the chat room can't see any previous messages (message history). We would have to implement that functionality for it to work that way.

## Screenshot

![screenshot](http://d.pr/i/15CQJ/4WxT350g+)
