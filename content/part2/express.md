# Express for our web server

So far we've created a Node script that prints something out to the terminal, which is great. Instead of doing that though, we need it to do something real.

In our case, we're building a web server, more specifically a _chat 'server'_. So we need to listen for incoming HTTP requests and then send down the HTML, CSS and JavaScript that we wrote earlier for our chat client.

While Node comes with basic HTTP handling support, a very (probably the most) popular 3rd party library (called "modules" in the Node community) named **Express** is used by most developers writing Web servers in Node. We shall use it too!

## Step 1

Let's install and save the Express library into our project by running this command from the command line that we have open.

```
npm install express
```

This downloads some code using the Node Package Manager (NPM) that we can use to make our lives easier.

![Install Express](/assets/install-express.png)

Now we can start using it. Type out the following JavaScript code into the **server.js** file.

```javascript
var express = require('express');
var app = express();

var http = require('http');
var server = http.Server(app);

app.use(express.static('client'));

server.listen(8080, function() {
  console.log('Chat server running');
});
```

### Explanation

So a bunch of new code and syntax was just introduced there. Let's attempt to break it down.

The first few lines are just loading external modules. We then tell the Express app to server all static content from the **client** folder.

When all the setup work is done, we then tell the server to listen in on a certain port (in this case 8080.)

So for now it's a simple web server serving only static (HTML, CSS and JavaScript) files to any HTTP/Web traffic coming its way. 

Let's try it out by running it using the same command as before.

```
node server.js
```

Now visit <http://localhost:8080> in your Web browser. It will bring up the chat app page just like before, with no new functionality. The send button should be working as before, too!
