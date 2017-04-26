# HTML
## The language of the Web

<a href="https://commons.wikimedia.org/wiki/File:HTML5_logo_and_wordmark.svg#/media/File:HTML5_logo_and_wordmark.svg"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/1200px-HTML5_logo_and_wordmark.svg.png" style="float: right" width=150px alt="HTML5 logo and wordmark.svg"></a>
No matter what anyone says, in order to be a serious web developer or even a competent computer scientist at any level or in any branch, some knowledge of HTML is a requirement.

The good news is, it's not really that hard.

## What is HTML
HTML is **HyperText Markup Language**. So what does that mean? When Tim Berners-Lee invented HTML back in the late 1980s, he was trying to make the concept of "hypertext" a reality. This is the idea that text doesn't have to be just static, unchanging ink on a page. In a book, when you read, you start at the first page and read left to right, top to bottom, front to back, page after page. And there's nothing wrong with that. However, hypertext means that the text is linked together in different ways. Pages are not one-after-another, but linked dynamically. Some words in the middle of a page might lead to [another page](introduction.md) in the book, or [another book entirely](http://www.wikipedia.org). When Berners-Lee sunk his teeth into hypertext, it was hardly a new idea. The idea of hypertext had been kicked around since the 1940s at least, and possibly a lot earlier. But HTML was the first truly widespread implementation of the concept. And it was so simple that it still exists today.

So what's a "markup language"? If you happen to be looking at this page on the web, go ahead and press **ctrl-u** on the keyboard. In most web browsers today, this should bring up the "page source", that is, the HTML that generated the page you are reading. In this page, if you scroll about halfway down, you should see this very text hidden amongst some codey-looking gibberish. That code is HTML. A "markup language" is a programming syntax that just "marks up" regular plain text. The browser looks at those markings and interprets them into formatting. HTML allows us to mark up text with formatting tags that create headings, paragraphs, lists, tables, and pictures in our websites.

<div class="alert alert-info">Note: This page was not originally written in HTML, it was written in another language called [Markdown](https://en.wikipedia.org/wiki/Markdown) which is--despite its name--also a markup language, thought quite a bit lighter weight and less feature-rich, but far, far faster to type and easier to read than HTML, but can then be parsed _into_ HTML.</div>

So HTML is a markup language to facilitate the generation of hypertext. It is the foundation of most of our interactive web-based media today. We are currently in HTML's 5th generation, generally referred to as HTML5. It was originally published by the [World Wide Web Consortium](https://en.wikipedia.org/wiki/World_Wide_Web_Consortium) in 2014 and has been the current version of HTMl since then. As far as this text is concerned, whenever we talk about HTML, we are specifically referring to HTML5.

## The HTML Tag

<div class="alert alert-info"><strong>A Word on Text Editors</strong>: When the text refers to text editors, it is vital to recognize that what a programmer refers to as an <strong>editor</strong> is very different from a <strong>Word Processor</strong>. Do <strong>not</strong> use Microsoft Word!! Feel free to download any text editor you like for local editing. There are as many text editors as there are programmers, it seems. But some nice modern ones to check out include <a href="https://notepad-plus-plus.org/">Notepad++</a>, <a href="https://www.sublimetext.com/">Sublime Text</a>, <a href="https://atom.io/">Atom</a>, and <a href="https://www.geany.org/">Geany</a>. If you are feeling adventurous, you can try some advanced text editors like <a href="http://www.vim.org/">Vim</a> or <a href="https://www.gnu.org/software/emacs/">Emacs</a>, but they have very steap learning curves. Such is the price of power and extensibility.<br> In case you're curious, this text was written largely on Atom in Vim mode.</div>

The basic unit of HTML syntax is the tag. Tags are meant to be _semantic_. What this means is, the tags you use should give some information about the meaning you are assigning to the text inside. A `<p>` tag indicates a paragraph as a unit of meaning. An `<h1>` tag indicates a high-level section heading. Different browsers treat tags slightly differently, but they do _mostly_ agree how to handle this tag or that. And whatever they don't can be picked up in **CSS** (more on that later).

Most HTML tags require a second tag to close it. The closing tag is always identical to the opening tag, only it comes with a forward slash. So a `<p>` tag and its closing `</p>` tag indicate that everything btween them is to be treated as a paragraph. Likewise, to create a heading in your html file, you will surround some text with `<h1>` and `</h1>`

To see this in action, create a text file using the simplest text editor you have

```html
<h1>Hello World</h1>
<p>Welcome to my web page</p>
<p>Stay as long as you like</p>
```
![1]

<!-- Images -->
[1]: images/1.png
