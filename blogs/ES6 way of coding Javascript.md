
# ES6 way of coding Javascript!
ECMAScript is the scripting language, and it forms the basis of JavaScript.
We'll look at the differences between its two versions, ES5 and ES6, today. 
ES6 is so far the best and biggest update javascript have ever received. 
It streamlined the javascript development and almost killed the jQuery's career.
& You'll see how ES6 allows us to write more legible, succinct, and efficient code throughout the article. Let's get started without further ado.



### ES5 WAY
`var element = document.getElementById('myForm')`

### ES6 WAY
>Use const if you don't want reassign the 'element variable by mistake.
`const element = document.getElementById('myForm')`
<hr>

### ES5 WAY
`function add(a,b){
return a+b
}
console.log(add(2,3))
//OUTPUT: 5`

### ES6 WAY
>Arrow function: write less do more! Arrow functions got introduced in ES6. This way of defining methods is concise and more readable. It does not require the keyword function, and sometimes not even return keyword and curly brackets.

`const add = (a,b) => a+b
console.log(add(2,3))
//OUTPUT: 5`
<hr>

### ES5 WAY
`var user= {
name "Hello World!",
username: "@hello"
}
const name = user.name
const username = user.username`

### ES6 WAY
>De structuring write less do more!

`var user = {
name "Hello World!",
username "@hello"
}
const {name, username} = user`