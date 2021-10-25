# Solution

### Challenge 1: ES5 to ES6

**Long version**
```js
const greetings = (name) => {
    return `Hello my name is ${name} !`;
}
```
_When there is only 1 parameter, it does not need to be contained in between brackets:_
```js
const greetings = name => {
    return `Hello my name is ${name} !`;
}
```

**Short version**
```js
const greetings = name => `Hello my name is ${name} !`;
```
---

**BONUS solution**
```js
const w = 'Nat'
let x = 'John';
let y = 'Marie';
let z = y;
y = x;
x = z;
console.log(`Here is ${z}, ${y} and ${w}`)
```