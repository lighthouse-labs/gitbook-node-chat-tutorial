# Express for our web server

So far we've created a Node script that prints something out to the terminal, which is great. Instead of doing that though, we need it to do something real.

In our case, we're building a web server, more specifically a _chat 'server'_. So we need to listen for incoming HTTP requests and then send down the HTML, CSS and JS that we wrote earlier for our _chat 'client'_.

While Node comes with basic HTTP handling support, a very (probably the most) popular 3rd party library (called "modules" in the Node community) named 'Express' is used by most developers writing web servers in Node. We shall use it too!

## Step 1

Let's install and save the Express library into our project by running the command.

`npm install express`

This downloads some code using the Node Package Manager (NPM) that we can use to make our lives easier.

![screenshot](http://d.pr/i/10kgL/2BlmzYbb+)

Now we can start using it. Type out the following JavaScript code into the `server.js` file.

```js
var express = require('express');
var app = express();

var http = require('http');
var server = http.Server(app);

app.use(express.static('client'));

server.listen(process.env.PORT, process.env.IP, function() {
  var addr = server.address();
  console.log("Chat server running at", addr.address + ":" + addr.port);
});
```

### Explanation

So a bunch of new code and syntax was just introduced there. Let's attempt to break it down.

The first few lines are just loading external modules. We then tell the Express app to server all static content from the `client` folder.

When all the setup work is done, we then tell the server to listen in on a certain port and IP address.

So for now it's a simple web server serving only static (HTML, CSS and JS) files to any HTTP/web traffic coming its way. 

Let's try it out by running it.

![screenshot](http://d.pr/i/1bz8V/4HQ3G3lz+)

Now visit the URL mentioned in the terminal output in another browser tab. It will bring up the chat app page just like before, with no new functionality. The send button should be working as before, too!

![screenshot](http://d.pr/i/23w5/1oxxdqvJ+)
