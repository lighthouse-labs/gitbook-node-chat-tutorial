# CSS

If HTML is the bread and butter of a web page, then CSS is our butter knife. Here's a picture of one, because, why not?

![screenshot](http://d.pr/i/1jmFc/2Ytr5fsx+)

Credit: Google Images

So why is CSS the knife? Well, it controls _what goes where_. Using CSS we declare how we'd like the content (HTML) to be presented.

More technically: CSS stands for Cascading Stylesheets, or something like that. The key word here is "style", something us Vancouverites generally lack. JK JK!

## Step 1

Let's prepare our HTML document to _link_ a stylesheet (`.css`) file to it. 

Add the following HTML tag _inside_ the `<head>` tag, ie right below/after the `<title>` element:

```html
  <link rel="stylesheet" type="text/css" href="style.css">
```

Now whenever this HTML file is loaded again, it will ask the browser to fetch another file (called `style.css`) from our web server and apply it to our HTML page. 

## Step 2

Oops, we don't even have that file in our project, let's add it using this again:

![screenshot](http://d.pr/i/1gxkO/3zpwIs1q+)

Call it `style.css`.

## Step 3

Inside the empty CSS file, add the code provided below. I would suggest that you type this out and do it incrementally (save and refresh the page to see the change after each major section instead of typing it all out at once).

Note: if no changes are reflected in the document (upon refreshing the page) then please confirm that your `<link>` tag is correct. Still a problem? Ask for help from your peers or a mentor.

```css
* { 
  margin: 0; 
  padding: 0; 
  box-sizing: border-box; 
}

body {
  font-family: 'Roboto Condensed', sans-serif;
  color: #244751;
  background-color: lightgray;
}

main {
  width: 450px;
  margin: 20px auto;
  background-color: white;
  border: 1px solid black;
}
```

The first section with the `*` is about normalizing the style so that it's consistent across all browsers (each has their slightly different default styling). Don't worry about it too much, it's a bit of _a hack_.

## Step 4

I'm actaully _not_ going to explain to you what this code is doing and how it's working, actually. Discuss amongst yourself and try and use your powers of reasoning, critical thinking and experimentation to solve the mysteries of CSS syntax. Look for patterns to help identify conventions and rules. HTML has its own completely different set of rules than CSS, but all languages have rules, and computer languages need strict rules. Use this to your benefit to deduce certain conclusions.

Also, feel free to google terms like [CSS background color](https://google.com/?q=CSS+background+color) or even [Please explain CSS bc Khurram won't!](https://www.bing.com/search?q="developers+developers+developers")

Also, the end result should look like something closer to what we're trying to get to, nice!

## Step 5 - A challenge

Using the following set of CSS properties, try to make the page look closer to this:

![final](http://d.pr/i/1k0TK/33fupKLm+)

First, add a few "line items" (eg: `<li>KV says: hello</li>`) within the `<ul>` element so that you have some content to work with.

### Properties

* `width`
* `background-color`
* `padding`
* `margin`
* `border`
* `font-size`

Feel free to google them up along with the keyword "CSS" to learn by example. StackOverflow, w3schools and MDN are all great resources that you'll likely end up on naturally. They tend to trend highest in results. 

BTW you'll likely need a few more CSS properties. Take your time :)

