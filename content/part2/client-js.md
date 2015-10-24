# JavaScript in the Browser

Let's add some behavior to your page so it works. That's where JavaScript or JS comes in.

## Step 1

Much like with the CSS, we need to link our new `.js` code with our web page, our `.html` content file.

Add the following HTML tag _inside_ the `<body>` element but right before it's closed off with `</body>`. It's not necessary but considered best practice to reference all the JS at the end of the page.

```html
<script src="https://code.jquery.com/jquery-1.11.1.js"></script>
<script src="app.js"></script>
```

Now whenever you refresh/load the web page, it will reference two separate JS files for the browser to download (at the end), one of which is external (3rd party) to our application. This 3rd party library called jQuery is there to make life easier. We don't _need_ it, but with it we can write less code. This is why most websites on the planet (Earth) use jQuery or other JS libraries like it.

## Step 2

The second file `app.js` needs to exist, so let's create it just like you created `style.css` earlier.

It will be empty at first, but let's add the following code into it:

```js
alert('hello from the JS file');
```

Save the file and refresh the (probably already running) html file in your other browser tab. Upon page load, you should see 


