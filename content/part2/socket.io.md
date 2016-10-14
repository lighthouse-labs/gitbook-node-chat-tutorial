# Socket.IO for Real-time messaging

Now it's time to add the last missing, yet crucial piece to our app: _chat functionality_!

To do this, we will leverage yet another 3rd party Node module. It's called Socket.io.

Check it out here: <http://socket.io/>.

Socket.io will leverage a more core technology that browsers give us called Web Sockets.

What's nice about Socket.io is that it will let us write similar JS code on both the client (browser) side and at the server (Node) side. 

## Step 1

Run the following command in the terminal window to install it on the server.
 
`npm install socket.io`

![screenshot](http://d.pr/i/17YCR/5L1xyxJ3+)

## Step 2

Now let's add some code in `server.js` that will use this library. This code block should be placed before/above `server.listen`.

```js
var io = require('socket.io')(server);

io.on('connection', function (socket) {
  socket.on('message', function (msg) {
    io.emit('message', msg);
  });
  socket.on('disconnect', function () {
    io.emit('message', "User disconnected");
  });
});
```

## Step 3

Next, we need to add similar logic to the client app.

Open the `index.html` file and modify the `script` tags below so that we also reference and make use of Socket.IO. We can do this by adding one more script tag before our `app.js`script tag, so that it looks like this down there.

```html
<script src="https://cdn.socket.io/socket.io-1.5.0.js"></script>
<script src="https://code.jquery.com/jquery-3.1.1.js"></script>
<script src="app.js"></script>
```

## Step 4

Open `app.js`, our client-side JS code file and let's add some code to send and receive messages from the browser.

Add the following code to the very top of the file.

```js
var socket = io();
```

This is saying that `socket` is now a reference to the SocketIO library.

## Step 5

In that same file, replace the `alert` line from before with the following code:

```js
  socket.emit('message', text);
  $('#m').val('');
```

The code above says to emit the textual message to the server instead of performing our temporary `alert` behavior. The second line in the code simply clears the input so that another message can be typed by the same user.

We're not done yet, we need to listen for messages that are received from the server and append them into the message list. Add the following code at the bottom of the file:

```js
socket.on('message', function (msg) {
  var incomingMessage = $('<li>').text(msg);
  $('#messages').append(incomingMessage);
});
```

This part tells the browser that any time a message is received from the real time web socket connection with the server, create a new `<li>` (list item) HTML element and append it to the messages `<ol>` (container).

## Final code for app.js

The `app.js` file should look like this.

```js
var socket = io();

$('form').submit(function () {
  var text = $('#m').val();
  socket.emit('message', text);
  $('#m').val('');
  return false;
});

socket.on('message', function (msg) {
  var incomingMessage = $('<li>').text(msg);
  $('#messages').append(incomingMessage);
});
```

## Final code for server.js

The `server.js` file should look like this:

```js
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
  socket.on('disconnect', function () {
    io.emit('message', "User disconnected");
  });
});

server.listen(process.env.PORT, process.env.IP, function () {
  var addr = server.address();
  console.log("Chat server running at", addr.address + ":" + addr.port);
});
```

## Whoa, it works!

Make sure all your files are saved, and the Node server is still running, and give it a shot.

That's right, it works! That's all it took. The basic chat functionality works. Have your peer go to the same URL that you're on and you guys should be able to communicate!

Note: newcomers to the chat room can't see any previous messages (message history). We would have to implement that functionality for it to work that way.

## Screenshot

![screenshot](http://d.pr/i/15CQJ/4WxT350g+)
