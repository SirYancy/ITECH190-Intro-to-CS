# Functions

<dl>
    <dt>Function</dt>
    <dd>A named block of code that can be called from another block of code. It always does the same thing. Depending on context, sometimes they are also called *methods*, or *subroutines*.</dd>
    <dt>Pseudo-random number</dt>
    <dd>Almost as good as random numbers, but not quite.</dd>
    <dt></dt>
    <dd></dd>
    <dt></dt>
    <dd></dd>
    <dt></dt>
    <dd></dd>
</dl>

What you will almost certainly discover as you progress as a programmer is that you will be repeating yourself. A lot. You will find yourself writing the same damned bit of code over and over and over again. And this is the problem that functions are designed to solve.

What if I could take that bit of code that I've typed a thousand times cut it out of the main part of my program and put it somewhere else and give it a name. And then my main program just calls that bit of code by its name in order to run it. To make things even more useful, I can feed that bit of code some sort of input and also get a result from it.

Every programming language has some way of defining and calling functions.

You've actually already called some functions. In the tip calculator, you called `parsefloat()` which is a built-in function that converts text into a floating-point number. This is a procedure that is common enough that it is built right into the language. 

Another function you've used a fair bit is `getElementById()`. This one is a little different because it has to be called *on* a document using what's often called **dot notation**. This is because the document is defined as the entire document that this javascript is being run in. Each element is *part* of that document and, if you happened to code in an **id** for an element, the `document.getElementById()` function can return that element to the program by feeding it the **id** that we're looking for. Thus, `document.getElementById('outputDiv')` will search through the document looking for an HTML element with the id "outputDiv" and if it finds it, it will return it to the code the called it.

## So What exactly _is_ a function?

A function is a named bit of code that you can use over and over. Functions have a couple of important features:

* **It's a black box** - A function's actual implementation (how the code is written) does not need to be known to the programmer to call it. In essence, it's a black box with an input and an output. Exactly what goes on inside that box doesn't matter as long as I know that the function works.
* **Same input -> Same output** - With a few notable exceptions (like random number generators), if you call a function with a certain input, should _always_ return the same output. If a function is supposed to add two numbers together and I feed it a 4 and a 5, it had better return 9 every time or else there's something wrong with the function.

## Whare they good for?

There are lots of reasons to write functions, but they can be distilled in a few essential ones:

1. They help us break a programming problem up into a series of discrete steps. Functions help us conceptualize our program as consisting of smaller sub-problems which makes the overall picture of the program easier to see.
1. Functions allow us to re-use code instead of rewriting it.
1. Functions give us the ability to test small parts of our programs in isolation from the rest of the program.
1. Functions allow us to control _scope_ and _encapsulation_. What this means is, we can create variables locally, within a function without them polluting the rest of our program. If I write a function where I want to add up all of the numbers in a list, I might create a variable to keep track of a running tally as I add each number. I only need this running tally number for the duration of that operation, after which, it can be tossed aside. By keeping it isolated in the function, the variable will be released after the function is finished and free up system resources.

We will elaborate and clarify some of these concepts throughout this section, but it is important to get some experience seeing these principles in action first.

## Functions in JavaScript

One important note about functions is that they *always* have trailing parentheses. These are for input. Whatever you want to pass to the function goes in here. If the function takes more than one **argument**, they will be separated by commas.

```javascript
myfunction(arg1, arg2);
```

JavaScript has many built-in functions. In this section, we'll learn a few more of those, and we'll also look at how to write our own functions.

Let's look at our first example

## Random Number Generator

Computers are actually not capable of true randomness. However, they can do a pretty good job of generating **pseudo-random** numbers. Most programming languages have a built in set of functions for doing math stuff and one of those is a pseudo-random number generator. Pseudo-random numbers are generated by a function that is passed a particular number or **seed**. And once it has a seed, it will keep on generating random numbers every time you call it. The funny thing is, if you pass it the same seed number over and over again, it will always generate the same sequence of "random" numbers. It's no longer very random if you know the seed. Most random number generators get around this problem by getting their seed from the system clock which is measured in milliseconds. It grabs the last few digits from the system time (which actually *is* pretty random) and then uses that as its seed. And it works pretty well for a lot of things. It's definitely just find for our purposes.

There are some random number generators that generate provably random numbers, but they are mathematically complex and rely on external input from static electromagnetic radiation in the atmosphere. [Random.org](https://www.random.org/) uses this method for generating its numbers.

JavaScript's RNG (random number generator) functions are to be found in its built-in Math module. There are a ton of useful math functions in the Math module. In fact, anything that's missing from the built-in operators (like exponents) can be found here. It wouldn't be a bad idea to look at a [list of everything in there](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math). But here's a rundown on some of the most popular ones:

| Method | Purpose |
| --- | --- |
| Math.random() | Returns a pseudo-random number between 0 and 1 (as a float) |
| Math.pow(x,y) | Returns *x* raised to the *y* power |
| Math.sqrt(x) | Returns the square root of *x* |
| Math.ceil(x) | Returns the number, *x*, rounded up to the nearest whole number (eg, 1.5 becomes 2) |
| Math.floor(x) | Reuturns the number , *x*, rounded down to the nearest whole number ( gh, 1.5 becomes 1) |
| Math.abs(x) | Returns the absolute value of *x* |