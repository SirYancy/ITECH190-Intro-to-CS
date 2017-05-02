# HTML Tags

<div class="alert alert-info"><strong>A Word on Text Editors</strong>: When the text refers to text editors, it is vital to recognize that what a programmer refers to as an <strong>editor</strong> is very different from a <strong>Word Processor</strong>. Do <strong>not</strong> use Microsoft Word!! Feel free to download any text editor you like for local editing. There are as many text editors as there are programmers, it seems. But some nice modern ones to check out include <a href="https://notepad-plus-plus.org/">Notepad++</a>, <a href="https://www.sublimetext.com/">Sublime Text</a>, <a href="https://atom.io/">Atom</a>, and <a href="https://www.geany.org/">Geany</a>. If you are feeling adventurous, you can try some advanced text editors like <a href="http://www.vim.org/">Vim</a> or <a href="https://www.gnu.org/software/emacs/">Emacs</a>, but they have very steap learning curves. Such is the price of power and extensibility.<br> In case you're curious, this text was written largely on Atom in Vim mode.</div>

## Basic Tags

The basic unit of HTML syntax is the tag. Tags are meant to be _semantic_. What this means is, the tags you use should give some information about the meaning you are assigning to the text inside. A `<p>` tag indicates a paragraph as a unit of meaning. An `<h1>` tag indicates a high-level section heading. Different browsers treat tags slightly differently, but they do _mostly_ agree how to handle this tag or that. And whatever they don't can be picked up in **CSS** (more on that later).

Most HTML tags require a second tag to close it. The closing tag is always identical to the opening tag, only it comes with a forward slash. So a `<p>` tag and its closing `</p>` tag indicate that everything btween them is to be treated as a paragraph. Likewise, to create a heading in your html file, you will surround some text with `<h1>` and `</h1>`

To see this in action, create a text file using a text editor (refer to "**A Word on Text Editors**" above if your instinct is to open Microsoft Word). Create a file called mywebpage.html and type out the following text.

```html
<h1>Hello World</h1>
<p>Welcome to my web page</p>
<p>Stay as long as you like</p>
```

Save the file and then navigate to the file. Double-clicking the file should open it in your default web browser and you will see the following. Your first web page:

![1]

Notice, that the `<h1>` tag tells the web browser to format the first line as large heading text. The `<p>` tag formats text as block-style paragraphs. To see the full effect of the paragraph tag, remove them and reload the web browser:

```html
<h1>Hello World</h1>
Welcome to my web page
Stay as long as you like
```

![2]

The paragraphs went away. In fact your web browser will strip away any white space that is not explicitly added. Extra spaces and new lines will be stripped out of your web page. The `<p>` tag allows you to semantically define your paragraphs instead of having to pay attention to exactly where your new lines are and your paragraphs end.

It's also worth noting here that HTML5 tags are not case sensitive. However, as a matter of code style, they are almost always lower-case. Using upper-case tags is archaic and to be frowned upon in this civilized era.

## Headings

Heading tags come in a variety of flavors. Those flavors are numbered according to their priority and web browsers will interpret them appropriately:

```html
<h1>Level 1 Heading</h1>
<h2>Level 2 Heading</h2>
<h3>Level 3 Heading</h3>
<h4>Level 4 Heading</h4>
<h5>Level 5 Heading</h5>
<h6>Level 6 Heading</h6>
<p>This is a paragraph</p>
```

![3]

## Basic Semantic Styling

Let's look at a quick rundown of some of the basic semantic tags that HTML has to offer:

|Tag|Effect|
|---|---|
|`<p></p>`|Defines a paragraph|
|`<h1></h1>` through `<h6></h6>`| Defines a heading|
|`<strong></strong>`|Strong Emphasis (bold)|
|`<em></em>`|Emphasis (italic)|
|`<br />` | Defines a line break (note the `<br>` tag closes itself)|
|`<hr />` | Defines a horizontal rule or line (closes itself)|

These are all fairly straightforward. Try some of these tags out in a simple html file.

```html
<h1>Welcome to my HTML tests</h1>
<p>This is a paragraph</p>
<p>
    This is also a paragraph,<br />
     But it has a line break
</p>
<p>
    I <strong>strongly</strong> disagree that HTML is <em>hard to learn</em>.
</p>
<hr />
<p>
    Come back anytime.
</p>
```
![4]

To see some more examples, go to the [demos] page. On any of the linked demo pages just hit `ctrl-u` to open a new tab with the source code for the page. Glance through them and you will see some things that we haven't covered yet, but we will in next few pages.

# What's Semantics, Exactly?

A few words on the term "**semantics**" is in order. HTML was designed, back in the day, as a way of giving very plain text some sense of style. This enhances readability, makes it look nice on the page, and gives the page structure. These days, there is a very strong emphasis on using so-called "semantic" HTML which emaphasizes the _meaning_ of information on the webpages as opposed to just defining what it should look like

For example, these days, it's preferable to use the `<em>` instead of the older `<i>` tag to create italic text. Rather than just saying it's italic, we're using the tag to denote an _emphasis_, and the use of the `<strong` tag instead of `<b>` for bold, strong text.

Semantic markup has been included in HTML since the very beginning, but since HTML4, and now much more in HTML5, this is only more pronounced and indeed, this is the general methodology that this text encourages as well.

<!-- Links -->
[demos]: http://itech190.erickuha.com/

<!-- Images -->
[1]: images/1.png
[2]: images/2.png
[3]: images/3.png
[4]: images/4.png
