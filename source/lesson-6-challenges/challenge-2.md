# Challenge 1: ES5 to ES6

This code is written in ES5. 
Using your newfound JavaScript knowledge, try to refactor these small functions in ES6 and output the same results.

#### Define a function `greetings` that returns `Hello my name is Sarah!`
```js
function greetings(name) {
    return 'Hello my name is' + name + '!'
}
greetings('Sarah')
```
---
**BONUS**
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

_In these exercises, we add a special bonus to go a bit further than the lesson... Have a look about a new ES6 concept: [the template literals and variables substitutions](https://www.w3schools.com/js/js_string_templates.asp)._
