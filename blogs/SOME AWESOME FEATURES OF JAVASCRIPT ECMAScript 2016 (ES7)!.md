![hashnode1.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1646334953806/cUm8SKUmj.png)
# SOME AWESOME FEATURES OF JAVASCRIPT ECMAScript 2016 (ES7)!


Javascript ES7 was a cake on top of the ES6 update. In my previous blog [ES6 way of coding Javascript!](https://wordssaysalot.hashnode.dev/es6-way-of-coding-javascript) , I discussed a few useful features that were added to JavaScript in order to make our lives easier and they certainly do. Now, Let's have a look at some of the features that ES7 has to offer!


## EXPONENTIATION OPERATOR
The exponentiation operator, **, was introduced in ECMAScript 2016(ES7).
Performs exponential calculation on operands, Same algorithm as Math.pow(x, y). It returns the first argument raised to the power of the second argument.

With ES7 with can do ( base** power )

```
const value = 2**5
console.log(value) //32
```


## ASYNC FUNCTIONS
ES7 given us the way to make any function 'asynchronous' explicitly. Very useful when we want wait for asynchronous request like http request, setTimeout etc.

```
function wait(){
   return new Promise((res, rej) => setTimeout(res, 2000));
}
async function asyncMania(){
   console.log("1"); 
   await wait();   /// It will wait for promise to get resolve 
   console.log("2");
}
```

## Array.prototype.includes()

Surprised right? Yes the include() method in Array was introduced with ES7.
Used for checking if the given element is in array or not.

Array.prototype.includes() checks the array for the value passed as an argument. If the array contains the value, it returns true; otherwise, it returns false.

```
const arr = ['Hello', 'World', '!']
console.log( arr.includes('Hello') )        //true
console.log( arr.includes('Hello !!') )    // false
```

## Object.entries()
Takes an object as parameter and returns a Array of arrays of key, value pairs.

```
const myObj = {name: "Ritesh Kumar", username: "@wordsaysalot"}
console.log( Object.entries(myObj) )

//OUTPUT
//[ ['name', 'Ritesh kumar'], ['username', '@wordsaysalot'] ]
```


## Add Paddings in String !
String.prototype.padStart() and String.prototype.padEnd() allows you to add padding to the string towards left and right side.

```
const myStr = "Hello"

console.log( myStr.padStart(10) )  //"_________Hello"
console.log( myStr.padEnd(10) )   // "Hello__________"

console.log( myStr.padStart(10, 'tests')) // "testsHello"
console.log( myStr.padEnd(10, 'tests'))   //  "Hellotests"
```

## Trailing commas
Last but not the least :) You can have trailing commas in function parameters.

```
const myfun = (a,b,c,)=> console.log(a,b,c)
myfun(1,2,3)    //OUTPUT: 1 2 3
```

### Conclusion
Over time, JavaScript has grown in popularity, and its community is continuously expanding. I tried to cover some of the key features brought to JS by ES7, but there is always more to learn.<br>
**Thanks for reading the article! I hope you guys found this article useful.**