# JavaScript in the Browser

Let's add some behavior to your web page so it works. That's where JavaScript (JS) comes in.

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

Save the file and refresh the (probably already running) html file in your other browser tab. Upon page load, you should see an alert pop up that says your message:

![screenshot](http://d.pr/i/1iOIM/1t9ilpa9+)

`alert` is a built in function that all browsers support, even though they may look slightly different on each browser. I'm guessing it's not your first time seeing one, so now you know how they happen.

Any time you call a function in JS you have to use `(parenthesis)` after it, and within the brackets you put in data that you want to give the function. Programming functions are much like math functions. They take in values and can do some crunching and give you back a computed value, or in this case, give you back some behavior like popup that message you passed into it.

Every single pre-defined JS function has documentation, so we can look up details about how they work. [Case in point](https://developer.mozilla.org/en-US/docs/Web/API/Window/alert).

Very soon, we'll create our own function while using other functions. It's going to get a bit more real, so hold on to your suspenders!

## Step 3

Remove the `alert` code and let's get down to business. We want to make it so when our `<form>` is submitted (via enter key or by clicking the send button), we read the text content in the 2 input fields (`id`'d as `m` and `you` in the HTML file) and do something with it, for now let's just `alert` it.

```js
$('form').submit(function() {
  var text = $('#m').val();
  alert(text);
  return false;
});
```

Remember, type that out yourself, don't copy paste it. Assuming you started and closed all the brackets, quotes, semicolons, etc correctly, it should add some interesting behavior to the page. 

Save the file, and refresh the html page. Put in some text into the second field and hit enter or click Send. You should see it echoed back to you in an alert message. If not, review or otherwise seek help ;)

![example](http://d.pr/i/1dJ6W/mKRvFgKR+)

### Explanation

The code above isn't doing too much, but it does need to be reviewed before we move on, don't ya think?

First, we use `jQuery` using the `$` function, telling it that we want to target all `form` elements on the page. There is only one form element on the page and it is the one at the bottom which contains both input fields and the button.

BTW note how we don't use the `<`angle`>` brackets when targetting elements here, just like with CSS. Angle brackets are solely used to _define_ tags in the html page.

Anyway, we then call/invoke another function called `submit` on that returned form element, saying that we want to be notified anytime that form is submitted.

In order to be notified any time this happens, we pass in our own custom function into the `submit` function. That's right, `submit` is a function that accepts a function. Read that again. Look at the code. Remember that we pass in data into functions within the `(`parenthesis`)`. They're not on the same line, but they are there.

This part may be a bit confused, so call over a mentor if you need.

Inside our function, the rest of the code is indented so that we know that it is within that function, just like we nest html tags with indentation (make sure your code is indented correctly because improper indentation is a big source of confusion).

This inside code is capturing the text value of the html element `id`'d as `m` and then passing it to `alert` so that we can see it. Tres cool.

The `return false` is there to tell the browser to cancel the original form submission logic (which is to attempt sending the form to the server, with loading spinner and everything). This is common practice when adding custom behavior to forms like we are doing here.










