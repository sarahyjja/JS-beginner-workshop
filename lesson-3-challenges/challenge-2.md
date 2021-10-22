# Challenge 1: ES5 to ES6

This code is written in ES5. 
Using your newfound JavaScript knowledge, try to refactor these small functions in ES6 and output the same results.

#### Which value does `w, x, y, z` have after execution of the following code?
```js
var w = 'Ella'
var x = 'John';
var y = 'Marie';
var z = y;
y = x;
x = z;
console.log('Here is ' + z + ', ' + y + ' and ' + w )
```
---
#### Define a function `greetings` that returns `Hello my name is Sarah!`
```js
function greetings(name) {
    return 'Hello my name is' + name + '!'
}
greetings('Sarah')
```