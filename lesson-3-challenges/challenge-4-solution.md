# Solution

### Challenge 3: Famous Writers

**Long solution with a `for loop`**
```js
for (var person = 0; person < writers.length; person++) {
    var firstName = writers[person].firstName
    var lastName = writers[person].lastName
    var age = writers[person].age
    var occupation = writers[person].occupation

    console.log(`Hi, my name is ${firstName} ${lastName}. I am ${age} years old, and work as a ${occupation}.`);
}
```
---
**Short solution with `forEach`**
```js
var whoAmI = writers.forEach(person =>
    console.log(`Hi, my name is ${person.firstName} ${person.lastName}. I am ${person.age} years old, and work as a ${person.occupation}.`))
}
```
_[Here](https://www.w3schools.com/jsref/jsref_foreach.asp) some documentation about it._

---
**BONUS solution**
```js
var aliveWriters = writers.forEach(person =>
    person.alive ? console.log(`I am ${person.firstName} and I am alive!`) : false)
```