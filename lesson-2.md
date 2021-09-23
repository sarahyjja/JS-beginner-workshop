# Lesson 2: JavaScript and the Command Line

## Introduction for this lesson

### Objectives

In this tutorial we are going to look at:

* what a command line is
* how to use the command line to navigate the file system and run programs
* what JavaScript is
* numbers and strings
* how to use variables
* calling and defining methods

### Goal

By the end of this tutorial you will have learnt how to navigate through the command line and how to run some basic operations in JavaScript.

## Introduction to the command line

### What is the command line?

The command line is a text interface for your computer. Similar to Windows Explorer on Windows or Finder on a Mac, it lets you navigate through the files and folders of your computer - but it is completely text based. The command line works by typing commands against a prompt, which then gets passed to the operating system of the computer that runs these commands.

### How do I access the command line?

On a Mac you can access the command line by opening the Terminal application
from the Applications > Utilities folder (or use `cmd (⌘) + space` and search
for "Terminal").

The command line can seem unfamiliar and scary, but it's really a different way of interacting with your computer. This tutorial only covers safe commands that will not do anything bad to your computer, even if you get them wrong.

### Navigating around in the terminal

Once you've opened up your terminal you should see a window that has says "Last login" with a date after it, and a cursor next to a dollar sign.

![](/images/lesson-2/image1.png)

Do not worry if the text in yours is a little different - it does not matter.

Basic commands are written on a single line, and run when you press the `Enter` button on your keyboard.

Try typing, then pressing `Enter`:

```shell
pwd
```

#### `pwd` or print working directory

The `pwd` command prints to the command line the current directory (another name for folder) you are in. If you have just opened up your terminal, you are probably in your "home" directory, and should get an output similar to this:

```
/Users/your-username
```

So your current "working directory" is `/Users/your-username`.

#### Getting things wrong on the command line

If you type a command that the command line does not understand, it will show you an error message. Do not panic if you see one of these - everything is fine! Take a look at the command you wrote and see if you can work out what was wrong.

Try this for example:

```shell
whargleblargle
```

You should see an error message like `-bash: whargleblargle: command not found`.

If you want to cancel your current entry, you can either delete the command using the backspace button, or press `Ctrl + C` to get a brand new line.  Your mouse will not work for navigating around the command line commands - but you can use the arrow keys on your keyboard to move the cursor left and right.

#### `ls` or list

You might wonder "how I do know which files are in a directory?", the `ls` command can do this:

```shell
ls
```

This should print a list of the files and folders inside the working
directory. You'll probably see directories like `Applications`, `Desktop`,
`Documents` and `Downloads`.

### `cd` or change directory

The `cd` command allows you to move between directories. You tell `cd` which directory to move to by putting the path after the `cd`, like this:

```shell
cd Desktop
```

Lots of commands need parameters like this - for example, `cd` needs to know the directory to move to, while `pwd` does not. We call the parameters "arguments".

### Task 1: change to the directory containing your code

In Lesson 1 we created a folder to keep our source code
(`lesson-1-html-and-css`). Create a new folder for lesson 2 called
`lesson-2-JavaScript` and change the working directory in your command line using
`cd`.

Confirm you're in the right place by running:

```shell
pwd
```

and check what files there are in this directory by running:

```shell
ls
```

There probably will not be any files because we have not created any yet.

#### Notes

In Finder you can copy the path to a directory by right clicking, holding
down the option key (`⌥`), and choosing *Copy "Directory" as Pathname*.
Alternatively, you can drag the folder onto the terminal and it will type
the path for you.

If your directory includes spaces (or other weird characters) you might
need to put it in quotes so the command line does not get confused. So:

```bash
$ cd '/Users/your-username/My Directory With Spaces/lesson-2-javascript'
```

instead of

```bash
$ cd /Users/your-username/My Directory With Spaces/lesson-2-javascript
```

## Introduction to JavaScript


### Running JavaScript interactively with Repl.it
As you write code, you'll want to be able to see what it does. For this, you need to "run it" somewhere. You can do this in a number of ways, but to keep things simple today, we are going to use a tool called [Repl.it](https://replit.com/).

- Create an account using your email address.
- Click the 'Create Repl' button in the top left hand corner to start a new project.
- Under the 'Template' drop down, make sure to select 'Node.js' as your language of choice
- Under the 'Privacy' title ensure your Repl is public, this will allow you to share your code with others if you'd like to.
- Click the 'Create Repl' button

You should now have your own coding playground to play with!

<div style="border: 1px solid grey;">
<img src="source/images/lesson-2/repl-complete.png" alt="Repl website, showing 'Hello World!' in the console">
</div>


### Hello World!
It is programming tradition that we begin our coding journey by running 'Hello World!' in our language of choice. So this will be the first thing we do in JavaScript using something called a `console.log()`.

The "console" is where you can see the output of your code. In Repl, you should see a console on the right.

We want to print "Hello world!" to the console. Thankfully in JavaScript there is a built-in way to do this, using a `console.log()`. You just need to put any text inside quotes, inside the parentheses, and when you run the code you should see that text printed to the console.

Try it out
Write this in your Repl:

```
console.log('Hello world!');
```

Click "run" and check the console. You should see "Hello world!" printed out on the right hand side. It'll look something like this:

<div style="border: 1px solid grey;">
<img src="source/images/lesson-2/js-hello-world.png" alt="Repl website, showing 'Hello World!' in the console">
</div>

You also might be wondering why there's a semicolon at the end of the code you wrote. Semicolons are used at the end of every statement in JavaScript. The code usually won't break if you forget it, but it's good practice to remember.
### Numbers

We can use JavaScript as a kind of calculator. Try typing `console.log(1 + 1)` into repl and click "run". Do you get the right answer?

In JavaScript, the `+` operator adds numbers together. Other operators include:

* `-` - subtract
* `*` - multiply
* `/` - divide
* `**` - raise to the power of

You can also use brackets (`()`) to group things, e.g. `(2 + 2) / 2` which would evaluate to 2, rather than `2 + 2 / 2` which would evaluate to 3.

#### Task 2: Maths challenge

Use Repl.it to work out the answer to "191 multiplied by 7".

<details>
<summary>Answer</summary>

```
console.log(191 *7);
=> 1337
```

</details>

### Strings

In the real world strings tie things up. Programming strings have *nothing*
to do with real-world strings.

Programming strings are used to store collections of letters and numbers.
That could be a single letter like `"a"`, a word like `"hi"`, or a sentence like
`"Hello my friends."`.

A JavaScript string is written as a quote (`"`) followed by some letters, numbers,
or symbols and ended with a closing quote (`"`). The shortest possible string
is called the empty string: `""`. It’s not uncommon for a single string to
contain paragraphs or even pages of text.

If you type a string into `irb` it will return it back at you:

```
irb(main):017:0> "Hello IRB"
=> "Hello IRB"
```

#### Getting things wrong in the code

Just like in the command line, if you give JavaScript a command it does not understand it will show you an error message. Again, do not panic! Everything is fine.

 JavaScript will do its best to explain why it did not understand your code, but sometimes the error messages can be hard for a beginner to understand.

For example:

```
console.log("Hello World!", hello);

=> ReferenceError: hello is not defined
    at /home/runner/TimeToCode/index.js:1:29
    at Script.runInContext (vm.js:130:18)
    at Object.<anonymous> (/run_dir/interp.js:209:20)
    at Module._compile (internal/modules/cjs/loader.js:999:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1027:10)
    at Module.load (internal/modules/cjs/loader.js:863:32)
    at Function.Module._load (internal/modules/cjs/loader.js:708:14)
    at Function.executeUserEntryPoint [as runMain] (internal/modules/run_main.js:60:12)
    at internal/main/run_main_module.js:17:47
```

Here, we are told that JavaScript does not know what to do with 'hello'.

### Variables

Programming is all about creating abstractions, and in order to create an
abstraction we must be able to assign names to things. Variables are a way of
creating a name for a piece of data.

Creating variables in JavaScript uses a single equals sign - `name` `=` `value`. Some examples:

```JavaScript
let name = "Fido"
let ageHumanYears = 4
let ageDogYears = ageHumanYears * 7
```

This would give three variables: `name` with a value of `"Fido"`, `ageHumanYears` with a value of `4` and `ageDogYears` with a value of `28`.

Variable names in JavaScript have to start with a letter, and they can not contain spaces or "special" characters like `-`, `$`, `@` and `&`.

As a style convention, JavaScript variables use capitalises the first letter of the next word to separate the bits of the name - this is called `camelCase` (as opposed to `snake_case` or `PascalCase` which are used elsewhere).

#### Task 3: Set and use a variable

Use Repl to set a variable called `answer` to the value of `7` multiplied by
`6`. Multiply the `answer` variable by `10` in Repl to see what happens.

<details>
  <summary>Answer</summary>

```
let answer = 7 * 6
console.log(answer)
console.log(answer * 10)
console.log(answer)

=> 42
=> 420
=> 42
```

</details>


### String Interpolation

We often need to build a string out of other strings and bits of JavaScript. In JavaScript we can do this with "template literals".

Within the string we use the interpolation marker(`). Inside those
backticks we can put any variables or JavaScript code which will be evaluated,
converted to a string, and output in that spot of the outer string.

```
console.log(`hello ${name}`)
=> hello Fido
```


#### Task 4: Use string interpolation

Using string interpolation in Repl, create a string with the text:

> "The answer to life, the universe and everything is ..."

Where `...` is the value of the `answer` variable you set in Task 3.

<details>
<summary>Answer</summary>

```
let answer = 7 * 6
console.log("The answer to life, the universe and everything is `${answer}`")

=> "The answer to life, the universe and everything is 42"
```

</details>


### Calling methods

While programming, we often find ourselves doing the same thing over and over again. It would be nice if we could give a particular task a name, and run it by calling its name.

In JavaScript we do this with *methods*, and there are lots of them already built into the language. One example is `Math.random()`, which generates a random number:

```
console.log(Math.random())
=> 0.46937366222850585
```


#### Task 5: Decode a secret message

