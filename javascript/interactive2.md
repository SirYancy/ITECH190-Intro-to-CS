# More Interactivity with JavaScript

We've primarily been playing around with string manipulation. The user enters some text information into a text box, we've been grabbing it, and then inserting it into some output. But now it's time for us to do some math.

## A Note Data Types

We've talked a little bit about data types already. There are four primary kinds of data types that you will learn about as you become a programmer, **strings**, **numerical types**, **booleans**, and **objects**. 

<dl>
    <dt>string</dt>
    <dd>A string is a data type that consists of a stream of text characters.</dd>
    <dt>Numerical Data</dt>
    <dd>Quite simply, a numerical type is a number. The two most common data types for our purposes will be ints and floats (more on this later in this section).</dd>
    <dt>Booleans</dt>
    <dd>A boolean is a data type with only two values, true or false. These are used for many things, but in this class, you will use them when you want your program to make a decision.</dd>
    <dt>Objects</dt>
    <dd>Technically all data types are objects, but usually when people talk about objects, they are referring to complex data structures that consist of many separate primitives. You can create your own objects and then create instances of them. Objects and object-oriented programming are somewhat outside the scope of thise course, but it is mentioned here for completeness. It cannot be stressed enough how important these will be down the road, however.</dd>
</dl>

JavaScript is a "dynamically typed" language which means that a variable can be any type at any time.In practice, however, when you create a variable and decide that it's a string, it should always be a string. There are almost no situations where you will want a string to suddenly become a number.

## Numerical Data Types

There are two primary numerical types that we will concern ourselves with and they're fairly straightforward. In most situations, JS handles these types automatically, but it is important that you get a firm understanding of the difference because it is a crucial distinction. Our two primary numerical data types are called **ints** and **floats**. 

An **int** is an integer. In case your algebra is a little rusty, and integer is simply any number without a fraction or decimal place. 5 is an int, as are -5, 36, -288, 7, and 42. Whenever you assign an integer value to a variable like `a = 42;`, JS automatically gives it the **int** type.

A **float** is short for "floating-point number". To keep it simple, a **float** is a decimal number. Any number with a decimal point like 1.2, 3.14159, 0.12, or even 5.0 is a float. The reason it's called a floating point number is that it can have any number of digits after the decimal point.

Why not just have floats? Well, doing math is complex. Designing circuits that can perform mathematical computations is tricky. While you could certainly just do all of your math using floating point numbers and using the circuits that perform those computations, it is far more taxing for the CPU. Integer math is far simpler to perform and reduces computational overhead. That is, it's quicker to use int when all you need is ints. We might be talking about nanoseconds, but over time, this can add up. An important principle of computer science is to the least amount of work in the most efficient way possible. Many, many brilliant minds have spent decades shaving tiny amounts of time from computer algorithms.

So, when you add two ints like `sum = 5 + 10;`, even if you don't notice it, it does take significantly less time and computer resources than adding to floats like `sum = 1.2 + 4.5;`.

That said, there is one other reason that ints are often preferable to floats. Floats are inaccurate. Look at this javascript shell session:

![4][4]

<span class="alert alert-info">In JavaScript (as with almost all other programming languages) the * character is the operator for multiplication. Mathematical operators will be discussed in more detail later in this section</span>

Notice anything weird? What is the product of 0.1 and 0.2? The answer should be, neatly, 0.02. But that's not the output of the multiplication in JS. And yet, the JS shell session outputs the very strange product `0.020000000000000004`. There are complicated reasons for why this is, but it all stems from the fact that at their core, all numbers are still binary and because of the way that floating point numbers are represented in binary leads to these strange little rounding errors.

Why, you ask, do they use floats if they behave this way? Well, for almost all applications, they are, frankly, good enough. It is, in the end, a _very_ tiny error. But it's still an error. For the purposes of this class, it's more a fun fact than something that you should be worried about. We'll mostly correct any errors like this by rounding.

## Mathematical Operators

There are four main mathematical operators in JS. They correspond to the four most common arithmetic operations: addition, subtraction, multiplication, and division. They are pretty straightforward, but in some cases, they are different from what you might be used to in normal mathematical notation:

| Operation      | Operator Symbol |
|----------------|-----------------|
| Addition       | +               |
| Subtraction    | -               |
| Mutliplication | *               |
| Division       | /               |

For now, this is all we'll need. They work in almost all the same ways that we're already familiar with in algebra.

Let's look at a couple of examples:

## Tip Calculator

Here's the code for a simple tip web page that calculates a 15% tip on a bill:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Tip Calculator</title>
</head>
<body>
    <h2>Tip Calculator</h2>
    <p>
        Enter the amount: $<input id="amountBox" size="10" type="text" />
        <br>
        Tip Percentage: 15%
    </p>
    <input type="button" value="Calculate Tip"
    onclick="
        amount = parseFloat(document.getElementById('amountBox').value);
        tip = amount * (15/100);
        document.getElementById('outputDiv').innerHTML = 
            '<p>You should tip $' + tip + '</p>';
    "/>
    <hr />
    <div id="outputDiv"></div>
</body>
</html>
```

You can play with a working version of this web page on the demo page. Click [here](http://itech190.erickuha.com/interactive_js/tip.html).

![5][5]

The program is quite simple upon a close inspection. Let's go through it. The page is a basic structure. The first `<p>` tag pair contains our main input, namely a textbox with the id "amountBox". The business, as usual, happens in the **onclick** attribute of the button. There are a couple of new things happening here.

First, instead of simply grabbing the value from the amount box with `document.getElementById('amountBox').value`, we are taking the result of that operation and feeding it into a function called `parseFloat()`. Remember that a text box is a container for text. As far as JavaScript is concerned, the value contained in that box is text. So if you put the value 25 in there, it doesn't see the number 25, but the string "25". What the `parseFloat()` function does is take that string and "read" it or "parse" it and try to turn it into a float. If it is successful, it the result of this line of code will be that the floating point value 25 will be stored in the **amount** variable. If you put something other than numerical data in the box, an error will be generated and the program won't output anything.

In the next line, we're just doing simple algebra. The value stored in amount is mutliplied by the value of (15/100), which is really just another way of expressing 0.15, or 15%. The reason for doing it this way will become clear in the next example. The result of this calculation is then stored in the variable **tip**. The reason for doing it this 

Lastly, we are generating a string value with the tip in the middle. Notice we don't need to do anything special to conver **tip** into a string. If you simply add the variable to a string, it will just become part of the string.

Neat, huh? Make sure you have a reasonable handle on what's going on here and then prepare to get your mind totally blown when you see this next slight variation of this program.

## Tip Calculator 2

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Tip Calculator 2</title>
</head>
<body>
    <h2>Tip Calculator 2</h2>
    <p>
    Enter the amount: $<input id="amountBox" size="10" type="text" />
    <br>
    Tip Percentage: <input id="percentBox" size="10" type="text" />%
    </p>
    <input type="button" value="Calculate Tip"
        onclick="
        amount = parseFloat(document.getElementById('amountBox').value);
        percent = parseFloat(document.getElementById('percentBox').value);
        tip = amount * (percent/100);
        document.getElementById('outputDiv').innerHTML = 
                         '<p>You should tip $' + tip + '</p>';
        "/>
    <hr />
    <div id="outputDiv"></div>
</body>
</html>
```
This version of the tip calculator should be quite simple to follow if you understood how the first one worked. The only real difference here is that we now have two input text boxes. In the `onclick` attribute, we have to grab the values of both elements, and then when we calculate the tip, we simply used the variable **percent** instead of the static 15. Note that here the reason for dividing our percent by 100 becomes clear. We can take the percentage and convert it into a decimal for making the calculation. Try to duplicate the code. A working version can be found on the [example page](http://itech190.erickuha.com/interactive_js/tip2.html).

## Coming up...

In the next section, we're going to look at how we can make re-usable code in our introduction to functions.


<!-- images -->
[4]: images/4.png
[5]: images/5.png
