# Node (JavaScript on the server)!

So far we've been building a web site with some static content and a bit of client-side interactivity.

It's time to take it up a notch and graduate to "web application" status. Server side app logic is what separates a site from an app.

## Step 1

First, stop the server if it's running:

![screenshot](http://d.pr/i/18zDg/2QUFHpkd+)

Let's then move all the "client" side files into their own folder called ... `client`.

![screenshot](http://d.pr/i/1jj5s/2uE8HilK+)

## Step 2

Switch focus to the "bash" command line terminal tab/window at the bottom by clicking on its tab, and initialize the project as a node application, by typing in `npm init -y`:

![screenshot](http://d.pr/i/ljXa/2V9uS9Ub+)

NPM by the way is a package manager for Node (Node Package Manager). It will be used later to install other packages into our app. 

## Step 3

Now let's add another javascript file to be run on the server side which will power the logic for our chat application. Call it `server.js` and put it at the top level (at the same level as the `client` folder):

In it, put this one test line of code, to log (aka output) a message to the screen, so we know that it is working:

```js
console.log('hello from our node script!');
```

![screenshot](http://d.pr/i/1j4Jg/2F7WTbb6+)

## Step 4

Let's run this bad boy. We'll use the Node runner given to us by Cloud9 to make life easy here:

![screenshot](http://d.pr/i/17Sx1/58mf36Nc+)

A new tab will open in the terminal panel at the bottom, which will say something very similar to:

```bash
Debugger listening on port 15454
hello from our node script!
```

And there's our message, nice!

You can click the red Stop button at this point.