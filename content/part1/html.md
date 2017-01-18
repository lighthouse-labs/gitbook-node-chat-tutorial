# HTML

HTML is the most fundamental language used on the Web. With it, we add information into documents that explain how they are linked together &mdash; that's how the Web works!

Now let's use it to build our app.

## Step 1

Create a folder on your computer to put the files for this project. A good name for the folder might be **Lighthouse Labs**. Then go to **File &gt; Open Folder...** and select your new folder. 

![Open Folder](/assets/open-folder.png)

You should now see an empty workspace ready for us to create our project in.

Create an new file in your project called **index.html** by right clicking the grey area on the left hand side.

![New File](/assets/new-file.png)

![index.html](/assets/index.html.png)

Open the file and add the following html code into it.

```html
<h1>hello, world</h1>
```

It should look like this.

![hello, world](/assets/hello-world.png)

Save the file and then navigate to your project folder and choose to open the **index.html** file in your Web browser. You'll get something like this.

![Hello, Chrome](/assets/hello-browser.png)

And that's it &mdash; you just built a Web page!

## Step 2

Let's build out the "markup" (structure) of our web page so it looks more like our goal, which is something like this.

![TODO]()

Here's a description of the what it contains.

1. A main area
2. Inside that there is the message history box
3. Inside the message history box is a list of messages
4. Below that is a form containing two input fields and a "Send" button. The first input field is for the initials of the person sending the message and the second is the message itself.

The initial HTML for this can be something like the following. Replace the content of **index.html** with this code. Please type it out instead of using copy and paste.

```html
<main>
  <ol id="history">
  </ol>
  <form>
    <input id="initials">
    <input id="message">
    <button>Send</button>
  </form>
</main>
```

Note a few important properties of HTML here.

### Tags define elements

Tags look like `<this>` and they have *meaning*. Examples of tags are `<p>` which means "paragraph" and `<h1>` means a "first level heading".

Most tags need an accompanying closing tag, for example `</p>` or `</h1>` after the text that goes inside the paragraph or heading.

### Nesting

We indent our code when that content is *inside* a tag (between opening and closing tags) so that it's easy to understand what code is inside other code. 

### IDs

We give `id`'s to certain elements so that they can be quickly referenced later.

This `id="something"` key-value pair that is part of an HTML tag is called an HTML attribute. Elements can have zero or more attributes. Attributes are cool and come in handy later.

## Step 3

Let's save and refresh the browser tab where the **index.html** file is open. It will hopefully look a lot like our final product.

![No style](/assets/no-styles.png)

Hm...not quite. Why does it appear this way and not like the example? 

We have provided the browser with a good understanding of the *structure* of our Web page, but not how to present it. The presentation rules are defined using another language called CSS.

## Questions?

If you have any questions about the above, flag me or another mentor so that we can answer any questions you may have.

Otherwise, it's time to move on to the next section.
