# Challenge 1: Age Difference

Write a function `ageDifference` that returns the difference in age between the oldest and youngest member of a family.

It should take two parameters: `youngest`, and `oldest`. These will always be objects. Use the following two as your test cases:

```js
var youngest = {
  name: 'Maya',
  age: 13
};
var oldest = {
  name: 'Joy',
  age: 83
};
```

Successfully calling the function will look like this:

```js
ageDifference(youngest, oldest); // ---> returns 70
```
---

# Challenge 2: Famous Writers

Did you know you can also have an array of objects? We've created one for you here. Loop through the array, and for each object, `console.log()` the following sentence:

```js
"Hi, my name is {firstName} {lastName}. I am {age} years old, and work as a {occupation}."
```

Ignore the brackets. They're just there to let you know a word should be replaced with something else. The sentence you log should look like this:

```js
"Hi, my name is Virginia Woolf. I am 59 years old, and work as a writer."
```

Here is the array:

```js
var writers = [
  {
    firstName: "Virginia",
    lastName: "Woolf",
    occupation: "writer",
    age: 59,
    alive: false
  },
  {
    firstName: "Zadie",
    lastName: "Smith",
    occupation: "writer",
    age: 41,
    alive: true
  },
  {
    firstName: "Jane",
    lastName: "Austen",
    occupation: "writer",
    age: 41,
    alive: false
  },
  {
    firstName: "bell",
    lastName: "hooks",
    occupation: "writer",
    age: 64,
    alive: true
  },
];
```

If you want an extra challenge, only `console.log()` the writers that are alive.

---
# Challenge 3: Fix the Code

The following code invokes a function called 'add' that adds two numbers together. When you run this code, it should add 13 to 27, and output '40' to the console.

But this code is broken! Using your newfound JavaScript knowledge, find the bugs and fix it.

```js
var first number = 13;
var second number = 27;
function 'add' () {
  return x + y;
}
add(first number, second number);
```

---

# Challenge 4: FizzBuzz

Write a for loop that prints the numbers from 1 to 100. But for multiples of 3 print “Fizz” instead of the number and for the multiples of 5 print “Buzz”. For numbers which are multiples of both 3 and 5 print “FizzBuzz”.

Counting to 15 should look like this:

```js
1
2
'Fizz'
4
'Buzz'
'Fizz'
7
8
'Fizz'
'Buzz'
11
'Fizz'
13
14
'FizzBuzz'
```

---

# Challenge 5: Needle in a Haystack

Can you find the needle in the haystack?

Write a function `findNeedle()` that takes an array full of junk, but containing one "needle", which you need to find with a for loop.

After your function finds the needle it should return a message (as a string) that says: `"Found the needle at position x"`, with `x` being the index number at which you find the needle.

So:

```js
var haystack = ['hay', 'rabbit', 'needle', 'hat'];
findNeedle(haystack);
```

Should return:

```js
'Found the needle at position 2'
```