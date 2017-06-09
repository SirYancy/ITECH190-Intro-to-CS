# The Variable

## Terminology

<dl>
    <dt>Variable</dt>
    <dd>A named container that stores a <strong>value</strong></dd>
    <dt>Value</dt>
    <dd>A number, string of characters, or other object that can be stored in a <strong>variable</strong>.</dd>
    <dt>Type</dt>
    <dd>A variable's type tells the computer how to interpret the binary information contained inside, such as an integer, a floating-point number, or a string of text.</dd>
</dl>

## What Is a Variable?

In computer science, the concept of a **variable** is pretty universal. You can think of it as a box that you put some value inside of for later use or for passing on to some other part of the program, like a function. What they allow us to do is write code that can be used more than once.

For example, I can add 7 + 3 in JavaScript and it will always output 10. But, if I want to add x + y, then x and y can be any values and their output could be anything as well. They could be dependent on user input, for instance, or contingent on some other result from elsewhere in the program.

So let's look at some of the basic properties that define a variable and rules that they must follow. 

1. A variable must be declared with a **name** - A variable doesn't exist until its named. This is true across the vast majority of programming languages. By declaring a variable, you instruct the interpreter to set aside a certain amount of space in memory for the variable and its value to reside.
1. A variable (usually) holds a **value** - A variable always has a value (at least in JS). JS does have two special values called "null" and "undefined" for variables that do not have other values, but these *are* actually JS primitive values. Besides *null* and *undefined*, the value stored in a variable can be a number, text string, a list, or some other complex data structure or object.
1. A variable cannot (usually) be used until it has been assigned a value - Often if a variable is declared but not defined, the interpreter will throw an error of some sort or the program will not behave as expected. JS is somewhat forgiving when it comes to this, but it's a good ideal to make sure that when you declare a variable, that you also assign it a value as soon as possible.
1. A variable has **scope** - A variable declared by a JS script in one web page will not affect a variable of the same name in another web page in another tab in your browser. This is related to a computer science concept called **encapsulation** which will be discussed later, but if you want to, it's a nice term to google.
1. A variable has a **type** - Since everything on a computer is encoded in 1s and 0s (binary), every variable needs to have a "type" which tells the computer what the bits inside mean. Some languages take typing more seriously than others. JS is a dynamically typed language which means that the type of a variable can change on the fly if the programmer needs it to.

## Creating and Changing Variables

As discussed in the previous secion, the **assignment operator** (=) is used to assign a value to a variable. If you wish to create a variable and assign it a value in one line of code, all you need to do is create a name for the variable, follow it with the assignment operator and then give it a value:

`x = 5;`

This assigns the value to the variable. using [SquareFree](http://www.squarefree.com/shell/shell.html), you can play around with these things. Try to duplicate this session in the JS shell of your choice:

![3]

<div class="alert alert-info">
<strong>Note</strong>I have been omitting the semicolons that terminate each line of code in the shell session. You really only need them when you are writing more than one line of code. In this very specific case, it's okay to leave them out.
</div>



<!-- Images -->
[3]: images/3.png
