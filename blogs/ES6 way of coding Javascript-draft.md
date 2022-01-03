![Blog banner](https://cdn.hashnode.com/res/hashnode/image/upload/v1641203757495/I6hzAb5Gx.png)
> Explore New Syntax in JavaScript ES6

JavaScript is an incredibly fast and efficient programming language to use for a variety of purposes. Today Every type of software uses JavaScript, including Web apps, 3D games, robots, IoT devices, etc.  
Back in 2007, Jeff Atwood (founder of StackOverflow), made a case that JavaScript would become a bigger part of web development. Atwood coined the term  `Atwood’s Law`, which states:


> Any application that can be written in JavaScript, will eventually be written in JavaScript.

It’s now ten years later, and Atwood’s statement is truer than ever. JavaScript is continuing to gain more and more adoption. The “next generation” of Javascript is something known as ES6. ES6 is so far the best and biggest update javascript has ever received. It streamlined the javascript development and almost killed jQuery's career. ES6 mainly allows you to write less code and do more.
In this post, I'll go over the six major differences between ES6 and ES5. Let’s take a look.

## Arrow function: write less do more
**ES5 WAY**

```
function add(a,b){ 
	return a+b
}
console.log(add(2,3))
//OUTPUT: 5
``` 
**ES6 WAY**
```
const add = (a,b)=> a+b
console.log(add(2,3))
//OUTPUT: 5
``` 
<hr>
## Use const if you don't want to reassign the 'element variable by mistake. 
**ES5 WAY**

```
var element = document.getElementById('myForm')
``` 

**ES6 WAY**

```
const element= document.getElementById('myForm')
``` 
 <hr>

## De-structuring: write less do more!
**ES5 WAY**

```
var user = {
	name "Ritesh Kumar", 
	username: "@0xRitesh"
}
const name = user.name
const username user.username
``` 

**ES6 WAY**

```
var user = {
	name "Ritesh Kumar".
	username: "@0xRitesh"
}
const {name,username} = user
``` 
 <hr>
## Template Literals
**ES5 WAY**

```
function getUsertMessage(name,country){
	console.log('Hi, my name is '+ name+ ',and I am from '+ country)
}
logUserMessage('Ritesh, 'India')
``` 
 
**ES6 WAY**
```
function logUserMessage(name,country){
	console.log(`Hi, my name is ${name}, and I am from ${country}`)
}
logUserMessage('Ritesh', 'India')
``` 
 <hr>
## improve Object Literals
**ES5 WAY**

```
function getUserObj ( name, age, address){
	return {
		name: name,
		age: age,
		address: address
		}
}
``` 

**ES6 WAY**

```
function getUserObj ( name, age, address){
	return {
		name,
		age,
		address
		}
}
``` 
 <hr>
## Default Parameters

**ES5 WAY**

```
function ES5Fun( username, platform){
	username, = username, || '@wordssaysalot';
	platform = platform || 'Hashnode';
}
``` 
**ES6 WAY**

```
function ES6Fun( username = '@wordssaysalot' , platform= 'Hashnode') {
}
``` 
### Conclusion
Thanks for reading the article! I hope you guys found this article useful, and I hope I was able to introduce you to some of the ES6 features. 





****
