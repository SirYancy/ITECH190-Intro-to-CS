# The Variable

## Terminology

<dl>
    <dt>Variable</dt>
    <dd>A named container that stores a <strong>value</strong></dd>
    <dt>Value</dt>
    <dd>A number, string of characters, or other object that can be stored in a <strong>variable</strong>.</dd>
</dl>

## What Is a Variable?

In computer science, the concept of a **variable** is pretty universal. You can think of it as a box that you put some value inside of for later use or for passing on to some other part of the program, like a function. What they allow us to do is write code that can be used more than once.

For example, I can add 7 + 3 in JavaScript and it will always output 10. But, if I want to add x + y, then x and y can be any values and their output could be anything as well. They could be dependent on user input, for instance, or contingent on some other result from elsewhere in the program.

So let's look at some of the basic properties that define a variable and rules that they must follow. 

1. A variable must be declared with a name - A variable doesn't exist until its named. This is true across the vast majority of programming languages. By declaring a variable, you instruct the interpreter to set aside a certain amount of space in memory for the variable and its value to reside.
1. A variable (usually) holds a value - A variable always has a value (at least in JS). JS does have two special values called "null" and "undefined" for variables that do not have other values, but these *are* actually JS primitive values. Besides *null* and *undefined*, the value stored in a variable can be a number, text string, a list, or some other complex data structure or object.
1. A variable cannot (usually) be used until it has been assigned a value - 
1. A variable has scope - A variable declared by a JS script in one web page will not affect a variable of the same name in another web page in another tab in your browser. This is related to a computer science concept called **encapsulation** which will be discussed later, but if you want to, it's a nice term to google.
