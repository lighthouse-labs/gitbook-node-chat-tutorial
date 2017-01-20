# Enhancements as Challenges (Stretch)

You may have noticed some bugs and broken features with this app.

## 1. Initial field - Part I

The initials input field (the first input box) is not being used at all. Modify the **app.js** so that it sends (emits) the text as something like `"DV says: hello"` where `"DV"` is from the first input field (with `id="initials"`) and `"hello"` is from the message field.

## 2. Initial field - Part II

The initials input field is actually meant to be 2 letter initials only. Make it so only a maximum of two characters can be entered into that field.

Hint: Google "html input field maximum length" for a convenient HTML attribute that can be added to your HTML file.

## 3. List of Messages

It would be nice to see the message history on the server anytime you join the chat room. Unfortunately, we don't keep/store a message history on the server at all. 

One way to do this is to create an empty [array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) that stores the messages. 

Then, whenever a message is received on the server, it can [push](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push) (append) that message string into the array.

Then whenever a user (new socket) connects to the server, (on `connection`) the server could iterate over all the messages in the array and `emit` them to that new client/socket.
