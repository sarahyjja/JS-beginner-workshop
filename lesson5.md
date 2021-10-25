# Lesson 5: If/Else Statements and For Loops

## If / Else
Now we're going to start adding in some logic. So far we have been logging the same thing every time we run the code, but what if we want to log different things according to different conditions? In programming there is something called an "if/else statement". It tests conditions, and will perform different actions based on the outcome of these tests.

The structure of an if/else statement in JavaScript is as follows:

```js
if (condition) {
  // do something
} else {
  // do something else
}
```

It basically translates to "if this condition is true, do this - or else do something else".

### Try it out

What if we want to `console.log()` "Hello world!" if we're feeling happy, and something else if we're sad?

Let's define a variable called `happy`, and assign it a boolean value of `true` or `false` (depending on how happy you're feeling).

```js
var happy = true;
```

Then let's write our if/else statement. In our condition, we want to test if the variable `happy` is equal to `true`. Note that in JavaScript, to test if two things are equal you need to use a triple equals (`===`) rather than just one (`=`). Read more about that [here](http://www.w3schools.com/js/js_operators.asp) if you're curious.

```js
if (happy === true) {
  // do something
} else {
  // do something else
}
```

Now let's add in what will happen if the conditions are met. The comments are there to explain what is happening.

```js
if (happy === true) {
  // if I am happy, print "Hello world!"
  console.log('Hello world!');
} else {
  // if I am sad, print a frowny face
  console.log(':(');
}
```

Now run this code (not forgetting to put the variable at the top of the Repl), and see what happens! Try changing the value of your variable from `true` to `false`.

---

#### Task 1 : Even or Odd

Write an if/else statement that evaluates if a number is even or odd. If it is even, it will print the string `'even'`, and if it is odd, it will print `'odd'`.

For this challenge, you might find it useful to use the "modulo" operator, which looks like this: `%`. The modulo operator finds the remainder after division of one number by another. For example:

```js
13 % 2 === 1 // 13 divided by 2 leaves a remainder of 1
100 % 10 === 0 // 100 divided by 10 leaves a remainder of 0
```

An even number will have a remainder of 0 when divided by 2. Read more about the modulo operator [here](http://www.w3schools.com/js/js_operators.asp).

<details>
<summary>Answer</summary>

```js
if(98 % 3 === 0){
    console.log('even')
} else {
    console.log('odd')
}
// => Should output 'odd'
```

</details>

---

### For Loops

Coding is great because it makes it easy to automate boring tasks, like writing the same thing over and over again. A "for loop" lets you do that in JavaScript. For loops basically let you perform the same operation a certain number of times, each time with a different value.

A for loop has the following syntax:

```js
for (statement 1; statement 2; statement 3) {
  // code to be executed
}
```

`Statement 1` defines a variable for the loop. 
It is usually a number, which we will increase each time the loop finishes, so we can keep track of where we're at. You can set the number to be whatever you want, but usually you will start at 0.

```js
var i = 0
```

`Statement 2` defines how long the loop will go on for. 
It most often uses the less than (`<`) or less than or equal to (`<=`) operators to set the length.

```js
i < 10
```

`Statement 3` defines how much to increment the `i` variable by each time. 
If you just want it to increase by one, then put `i++` (this is the shorthand for `i = i + 1`), or else you can increase by other numbers like so:

```js
i += 2 // this is the shorthand for i = i + 2
```

Inside the curly brackets goes the code you wish to be executed each time the loop runs. You can refer to the variable `i` from inside the loop.

### Try it out

Here's an example of an actual `for loop` that prints out the numbers 1 to 10:

```js
for (var i = 1; i <= 10; i++) {
  console.log(i);
}
```

Notice the variable `i` is set to `1`, because we want counting to begin at 1. The length is set to be less than or equal to 10, as we want the loop to end there. And we are increasing the value of `i` by one each time.

---

#### Task 2 : ForLoop

Write a `for loop` that loops over the numbers from 0 to 100, printing only every second number. So it should return `0, 2, 4, 6, 8, 10...`.

<details>
<summary>Answer</summary>

```js
for (var i = 0; i <= 100; i += 2) {
  console.log(i);
}
```

</details>