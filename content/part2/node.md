# Node (JavaScript on the server)!

So far we've been building a website with some static content and a bit of client-side interactivity.

It's time to take it up a notch and graduate to "Web application" status. Server-side app logic is what separates a site from an app.

## Step 1

Move all the "client" side files into their own folder called **client**.

![Client folder](/assets/client-folder.png)

## Step 2

Now let's add another JavaScript file to be run on the server side which will power the logic for our chat application. Call it **server.js** and put it at the top level (at the same level as the **client** folder.)

In it, put this one test line of code, to print a message to the screen so we know that it is working.

```javascript
console.log('hello from our node script!');
```

![Server test](/assets/server-test.png)

## Step 3

Let's run it. Open up the **Terminal** app on MacOS or **cmd.exe** on Windows to get to a command prompt.

Next you'll have to change the working directory to the one where your project files are. In the example below I used the commands:

```
cd Desktop
cd Lighthouse\ Labs
```

Then to run the file I did the command:

```
node server.js
```

The output should look like this.

![Terminal test](/assets/terminal-test.png)

And there's our message, nice!

