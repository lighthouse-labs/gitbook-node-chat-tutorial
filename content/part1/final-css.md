# Example CSS

There is no "one right solution" to CSS. There are many approaches to solving the same thing (admittedly in some cases there are some better than others) not to mention all the creative freedom you get with it.

That said, if you are looking for one possible CSS file so that you can move on, scroll on down! ... 

Oh hello....


![png](https://cl.ly/3m0W2P1J3B2F/Image%202016-09-26%20at%201.57.11%20PM.png "empty")


So,


![png](https://cl.ly/3m0W2P1J3B2F/Image%202016-09-26%20at%201.57.11%20PM.png "empty")


I'm intentionally leaving a LOT of white space here in case you didn't mean to see the spoiler.


![png](https://cl.ly/3m0W2P1J3B2F/Image%202016-09-26%20at%201.57.11%20PM.png "empty")


But, if you're ready to see the code, you're almost there...


![png](https://cl.ly/3m0W2P1J3B2F/Image%202016-09-26%20at%201.57.11%20PM.png "empty")


I said, almost.


![png](https://cl.ly/3m0W2P1J3B2F/Image%202016-09-26%20at%201.57.11%20PM.png "empty")


```css
* { 
  margin: 0; 
  padding: 0; 
  box-sizing: border-box; 
}

body {
  font-family: 'Roboto Condensed', sans-serif;
  margin: 0;
  color: #244751;
  background-color: lightgray;
}

main {
  width: 450px;
  margin: 20px auto;
  padding: 2em;
  background-color: white;
  border: 1px solid black;
  border-radius: 10px;
}

input[type=text] {
  border: solid 1px #244751;
  padding: .5em;
  font-size: 1em;
}

button {
  padding: .5em;
  background-color: white;
  border: solid 1px #244751;
  display: inline-block;
}

form {
  border-top: 1px solid black;
  margin-top: 10px;
  padding-top: 10px;
}

#you {
  width: 50px;
}

#m {
  width: 284px;
}

#messages { 
  list-style-type: none; 
  margin: 0; 
  padding: 0;
}

#messages li { 
  padding: 5px 10px;
  background: #ddd;
}

#messages li:nth-child(odd) { 
  background: #eee; 
}
```
