# What is JavaScript?

JavaScript is a programming language developed in the 90s. Unlike HTML, which is just a markup language, used to take plain text and give it structure, JavaScript is actually for writing programs.

Specifically, it is a **high-level**, **dynamic**, **interpreted**language.

## High-Level Language

JavaScript is a **high-level** language, which means that it is heavily abstracted away from the bare metal of the computer. In order to access the computer hardware, it relies on many systems and lots of software to get there. High-level languages are typically far easier to use and are often kind of like writing natural language, unlike machine language (which is just 1s and 0s) or assembly languages (which are *very* hard to read and understand).

High-level languages are where almost all computer scientists begin their explorations of software and computer systems. And many never really have much need to explore much deeper.

## Dynamic Language

High-level languages are written in human-friendly syntax. But what's good for a human to read, write, and understand is not necessarily so great for a computer. Remember, computers *only* understand 1s and 0s. Some high-level languages overcome this through the use of a compiler. That is, after you, the programmer, writes the program, it is run through *another* program called a compiler that translates it into machine language (or something closer to it).

Dynamic languages, on the other hand, are not compiled until they are run. They execute many of their behaviors at run-time. That is, it's just plain old code until the program is loaded into its **interpreter**. An interpreter is a piece of software that executes the code of a dynamic language.

## Why JavaScript?

So you might be asking, why should I learn JavaScript? There are two very good reasons for a new programmer to learn JavaScript.

**JavaScript is easy.** It requires no setup. All you need to run a JS program is a text editor and a web browser. It's simple to get into and the syntax is very straightforward. You can practically dive right in without downloading anything, installing an development environment, or getting to know weird new software.

**You're going to learn it anyway.** In all likelihood, if you're going to be a software developer, you will almost certainly need to develop at least some basic web development skill. That means, you need to know HTML/CSS, but it also means that you need to learn a little JavaScript.

## Text Editors and Web Browsers

You need two pieces of software to write JS programs. You need a text editor and a web browser. You probably already have a simple notepad program on your computer. It is important to note that a text editor is *not* a word processor. You absolutely should not use Microsoft Word. As stated in the HTML chapter, a few easy-to-use options are available completely free.

* [Sublime Text](https://www.sublimetext.com/) - Premium, but with an unlimited free trial. Extensible.
* [Notepad++](https://notepad-plus-plus.org/) - Windows only. very easy to use. extensible.
* [Atom](https://atom.io/) - All platforms. Totally free. Highly customizeable. Easy to use. Slightly buggy (it's pretty new on the scene)
* [Vim](http://www.vim.org/) - All platforms. Steep learning curve. Incredibly powerful. Almost certainly requires a few days of dedication to get the hang of it.

As for web browsers, you're probably using one right now to read this text. There are many pros and cons to each web browser and suffice to say, the author of this text has a tendency to jump back and forth between Chrome, Firefox and Opera.

## Try it out!

You're in your web browser right now, in all likelihood. And every web browser has a built-in JS console.

1. Open a new tab in your browser and point it to [SquareFree](http://www.squarefree.com/shell/shell.html). SquareFree is a simple JS **shell** which allows you to execute JS commands to see what they will do.
1. Now, press **Ctrl-Shift-J**. The browser's console log should appear. There may be some text already in it, you can igore it.
1. In the SquareFree shell, type `console.log("Hello World!");` and press **enter**.
1. Look over in your browser console and you should see it echo "Hello World!" back to you!

Neat, huh? Now, in most browsers, the JS console actually has its own prompt, but in some browsers (Firefox), it's disabled by default and has to be enabled by fiddling with the settings (google can help you here). So, you don't necessarily have to use SquareFree, but it's a nice tool that's easy to use.

## Write Your First Program

Let's turn this into its own standalone program. Open your favorite text editor. Create a file called `hello.html`. Type out the following code. Pay close attention to the syntax.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title></title>
</head>
<body>
<script>
    alert("Hello World!");
</script>
</body>
</html>
```
Navigate to the file in your file manager and double-click it. It should open in your default web browser and you should see something like this:

![1]

If you don't get the alert pop-up it could be one of two things. Either you made a mistake and should go back and check your syntax, or your browser has JavaScript disabled. To fix the latter, do a quick web search for it and your web browser and you should find a quick tutorial. This is, however, highly unlikely as the vast majority of web sites make heavy use of JS and if you had it disabled, you would almost certainly be aware of it.

Now, let's break down what we did. First, notice the `<script>` tags. Anything you put between these two tags will be interpreted by the web browser as JS and sent through the browser's built-in JS interpreter. The interpreter will take your JS code, in this case the single line `alert("Hello World!");`, parse it, and execute it. There are a few things you should pay close attention to in this single line of code. First, is the `alert()` keyword. This is a function built into JS that pops up an alert dialog box in the user's web browser with the message inside the parenthesis. The message is typically inside quotation marks. Lastly, the line of code must be terminated by a semicolon. In fact, all lines of JS code must terminate in a semicolon (more on this in the next session).

To close this section, try a few different variations on our "Hello World!" program. To try these examples, make the edit in the file, save it, and then refresh your web browser to test it.

* `alert("Hello" + " World!");`
* `alert(1 + 2 + 3 + 4 + 5);`
* `alert("1" + "2" + "3" + "4" + "5");`
* `confirm("Do you wish to continue?");`

<!-- images -->
[1]: images/1.png
