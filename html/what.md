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
The basic unit of HTML syntax is the tag.

```html
<p>This is a pargraph</p>
```
