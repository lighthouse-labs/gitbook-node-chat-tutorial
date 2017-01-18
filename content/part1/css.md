# CSS

If HTML is the bread and butter of a web page, then CSS is our butter knife.

Why is CSS the knife? Well, it controls _what goes where_. Using CSS we declare how we'd like the content (HTML) to be presented.

CSS stands for Cascading Stylesheets. The key word here is "style", referring to the way something _looks_.

## Step 1

Let's prepare our HTML document to _link_ a stylesheet (**.css**) file to it. 

Add the following HTML tag to the top of your **index.html** file and save it.

```html
<link rel="stylesheet" href="style.css">
```

When the HTML file is loaded again, it will ask the browser to fetch another file (called **style.css**) from the Web server and apply its rules to our HTML page.

## Step 2

Oops, we don't even have that file in our project, let's add it the same way we created the **index.html** file.

Make sure to call it **style.css** exactly as it is in the tag.

## Step 3

Inside the empty CSS file, add the code provided below. I would suggest that you type this out and do it incrementally (save and refresh the page to see the change after each major section instead of typing it all out at once.)

Note that if no changes are reflected in the webpage (upon refreshing the page) then please confirm that your `<link>` tag is correct. Still a problem? Ask for help from your peers or a mentor.

```css
body {
  background-color: white;
  color: #303030;
  font-family: 'Helvetica Neue', Arial, sans-serif;
}

main {
  max-width: 450px;
  padding: 20px;
}
```

## Step 4

I'm _not_ going to explain to you what this code is doing and how it's working. Discuss among yourself and try and use your powers of reasoning, critical thinking and experimentation to solve the mysteries of CSS syntax. Look for patterns to help identify conventions and rules. HTML has its own completely different set of rules from CSS, but all languages have rules, and computer languages need strict rules. Use this to your benefit to reason toward conclusions.

Also, feel free to Google terms like "[CSS background color](https://google.com/?q=CSS+background+color)".

The end result should look a little bit closer to what we're trying to get to.

## Step 5 - A challenge

Add a few "list items" (for example `<li>DV says: hey</li>`) within the `<ol>` element so that you have some fake messages that can be styled. Add at least four of these. They can be removed later when we get into JavaScript.

Now use CSS to try and make the page look closer to this.

![Example](/assets/example.png)

If you have time to spare, give it your own unique look. 

### Properties

Here is a list of CSS properties that you may want to try.

* `width`
* `background-color`
* `padding`
* `margin`
* `border`
* `border-radius`
* `font-size`

Feel free to Google them along with the keyword "CSS" to learn by example. StackOverflow, w3schools and MDN are all great resources that you'll likely end up on naturally. They tend to be highest in results. 

You'll likely need a few more CSS properties. Take your time. :)
