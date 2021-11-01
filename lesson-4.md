# Lesson 4: Arrays and Objects

## Arrays
It was mentioned earlier that there are data types other than strings, integers and booleans. An array is one of these. Arrays allow you to easily store multiple values together.

The syntax is to list the values separated by commas, inside square brackets:

```
[ "a", "b", "c" ]
```

You can store any type of value inside an array: strings, numbers, booleans. You can even store other arrays, or objects (which you will learn about next).

### Try it out
Defining an array as a variable looks something like this:

```
let animals = ["tiger", "puppy", "snake", "llama"];
```

 Now you have all the animals grouped together rather than having to define them separately. You can see how many animals there are by using `.length`:

```
console.log(animals.length);
```

If you want to refer to one specific member of the array, you can do so by using their "index number" like:

```
console.log(animals[1]);
```
Take a guess at which animal that will print out, and see if you're right.

Spoiler alert, it will print out "puppy". That might seem weird, until you learn that JavaScript is a "0-index" language. What that means is that counting in JavaScript starts at 0. So animals[0]will print out "tiger". We don't make the rules...

---

#### Task 1

How would you `console.log()` the name of every animal in the array?

If you're thinking of a for loop, you're right. This is the perfect opportunity to use our newfound for loop skills for a higher purpose.

Try googling to find the answer if you're stuck. Google skills are an essential part of being a developer.

<details>
<summary>Solution</summary>

```
let animals = ["tiger", "puppy", "snake", "llama"];

for (let i = 0; i < animals.length; i ++) {
  console.log(animals[i]);
};
```
</details>

---
## Objects

Now for the final data type, let's talk about Objects. Like arrays, they can store multiple bits of information, except objects store the properties of something. For example, you might want to save the name, model and colour of a car. Or the name, time and location of a film playing at the cinema.

The syntax looks like this:

```js
{
  property1: "value1",
  property2: "value2",
  property3: "value3"
}
```

The names on the left ("property1") are known as "keys". You can call them whenever you want, and any values can be given to them: strings, booleans, integers.

### Try it out

Let's define an object that represents a person:

```js
var person = {
  firstName: "Virginia",
  lastName: "Woolf",
  occupation: "writer",
  age: 59,
  alive: false
};
```

We can of course `console.log()` the entire object, but you can also reference just one of the properties. Run this code:

```js
console.log(person.firstName);
```
---
#### Task 2 : Try to manipulate an object.

Create an object representing a person. Then `console.log()` a simple sentence to introduce this person. Print out the following:

```js
"Hi, my name is {firstName} {lastName}. I am {age} years old, and work as a {occupation}."
```

<details>

<summary>Hint</summary>
<span>You can build a string by adding different strings and values together. To do it, you can use the concatenation operator "+". </span>
<span>Don't forget, you might need to include spaces.</span>
</details>

You can use the following example to help you:
```js
var animal = {
    species: "cat", 
    name: "Tabitha"
};
console.log("My " + animal.species + "is called " + animal.name + ".");
```
