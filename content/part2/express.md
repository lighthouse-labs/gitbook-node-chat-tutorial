# Express for our web server

So far we've created a node script that prints something out to the terminal, which is great. Instead of doing that though, we need it to do something real.

In our case, we're building a web server, more specifically a _chat 'server'_. So we need to listen for incoming HTTP requests and then send down the HTML, CSS and JS that we wrote earlier for our _chat 'client'_.

While Node comes with basic HTTP handling support, a very (probably the most) popular 3rd party library (called "modules" in the Node community) named 'Express'. 

## DYK!!

**That reminds me!** Since you've made it to this point, I guess you deserve a really juicy bit of DYK (did you know).

A very large part of the NodeJS ecosystem / codebase was actually written by a young fellow by then name of TJ Holowaychuk. He lives in Victoria, BC. 

![TJ](http://d.pr/i/1azN5/16iw08fD+)

Here's an [interesting blog post](https://medium.com/@kelas/how-is-tj-holowaychuk-so-insanely-productive-604818b4e9eb) talking about TJ. And here's a [Quora question](https://www.quora.com/How-did-TJ-Holowaychuk-learn-to-program) with a short discussion about him.

His code has made its way into a very very large number of software products that we use today. Here's an example that you may appreciate: [FreshGrade](https://www.freshgrade.com/), a very successful Kelowna based startup, uses NodeJS and Express ([example job post by them](http://freshgrade.applytojob.com/apply/3ANYBx/Senior-Backend-Developer-Nodejs-API-Craftsman)) and thus code that TJ wrote. The same is true for other bigger companies like LinkedIn, Apple, Google, Mozilla, AirBnB, WhatsApp, Instagram, etc etc. Amazing, huh?

## Step 1

Okay, so back to business.

Let's install and save express into our project by running the command: `npm install express --save`

![screenshot](http://d.pr/i/10kgL/2BlmzYbb+)







