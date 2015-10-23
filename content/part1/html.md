# HTML

HTML is short for Hotmail. No, just kidding. It's actually short for Hyper Text Markup Language. It's a fancy way of saying that we use "markup" text/english to annotate and describe the structure of our web page content. It's the bread and butter of every web site you've every visited.

So let's use it to build our app.

## Step 1

Create an new file in your project called `index.html` by right clicking the top level folder in the tree view on the left hand side.

![example](http://d.pr/i/WClH/2cnEeYM7+)

Open the file and add the following html code into it:

```html
<!doctype html>
<html>
  <head>
    <title>CUEBC Chat App!</title>
  </head>
  <body>
    Hello world!
  </body>
</html>
```

Save the file using <kbd>cmd</kbd> + <kbd>s</kbd> just like you would in any other text editor.

With this file selected on the left side, click the green "Run" button. You'll see a terminal output like the one shown below. Copy the highlighted URL and paste it into a new browser tab.

![example](http://d.pr/i/6Ffy/282MJmg1+)

Boom, you just built (your first?) HTML page!

Notice the URL, you can even have your team member / pair programmer put that URL in their browser and see the same results. It's online too?! Thank you Cloud9!

## Step 2

Let's build out the "markup" (structure) of our web page so it looks more like our goal, which is something like this:

![example](http://d.pr/i/1k0TK/33fupKLm+)

Here's a general english description of the contents, do you agree?

1. We have a main area (the main white rounded box) 
2. Inside that there is a message box
3. Inside the message box is a vertical list of messages with zebra-striping (alternating background colours)
4. Below that is a form containing two input fields and a Send button. The first input field is for two letter initials of who is sending the message and the second is the message itself.

The initial HTML for this can be something like the following. Type out this code (please type it out, no copy / paste!) in between the `<body>` and `</body>` lines:

```html
<main role="main">
  <ul id="messages">
  </ul>

  <form>
    <input id="you" type="text"></input>
    <input id="m" type="text"></input>
    <button>Send</button>
  </form>
</main>
```

Note a few important aspects to HTML here:

### A. Tags define Elements

Tags that look like `<this>` have _meaning_. Other examples of tags would be `<p>` for a paragraph and `<h1>` for a "Heading 1".

They are closed by an accompanying closing tag (eg: `</p>` or `</form>`).

### B. Nesting

We indent our code when that content is inside (within) some content so that it's easy on the eyes and we can understand what is going on. 

### C. IDs

We `id` certain elements so that they can be quickly referenced later.

This `id="some-identifier"` key-value pair located _inside_ an HTML tag is called an HTML attribute. Elements can have zero or more attributes. Attributes are cool and come in handy later (you'll see).

## Step 3

Okay now let's save and refresh the other tab where the `index.html` file is open and being displayed to the user. It will hopefully look a lot like our final product...

![example](http://d.pr/i/ZHBD/LlgXPLjH+)

Damnit! Not even close... sigh.

What gives? Well the browser has a good understanding of the _content_ of our webpage, but no idea about how to display it. The presentation rules are defined using another language, called CSS.

> Ugh, another language. Will it never end? 

Chin up soldier, this is fun!

## Questions?

If you have any questions about the above, flag me or another mentor so that we can answer any questions you may have.

Otherwise, move on to the next section.
