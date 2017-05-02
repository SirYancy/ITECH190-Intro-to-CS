# Hyperlinks

If there's one thing that truly defines hypertext, it is the hyperlink. The whole idea behind HTML and the web is the ability to link pages together. A traditional book (no offense to tradiitonal media!) is read front to back, left to right. The closest thing to a hypertext-like experience is a table of contents or an index, and even then, you still have to flip through the pages manually.

With HTML and the Web, however, you can link directly from one web page to another, even on another web site with ease. I can link to another page in [this book] or I could even link straight to [Google] or [Wikipedia]. The syntax for this is a little tricky, but let's break it down.

## The Anchor Tag

The tag that allows hyperlinking is called the Anchor tag, `<a>`. There are several uses for the anchor tag, but its most important job is creating links between pages. First, let's see a link in syntax and then we'll explore how it works.

```html
Here is a link to <a href="http://www.wikipedia.org">Wikipedia</a>
```

This renders to this: <br /> ![9]

Here's how it works. The anchor tag pair `<a></a>` surround the display text. This _semantically_ designates the word "Wikpedia" as a link. But the link won't work without some way of creating the link. Thus, the opening tag has an attribute called `href`. The `href` attribute takes the **URL** for the Web page or other resource that you are linking to.

## Relative vs Absolute Links

Web pages, behind the scenes, have directory structures just like your computer's file manager. There are folders that contain html files, images files, stylesheets, and whatever else your web page my need to do its thing. Imagine you have a website with the following file structure.

```
├── www/
│    index.html
│   ├── images/
│   │   ├── panda.jpg
│   │   ├── pangolin.png
│   ├── colors/
│   │   ├── red.html
│   │   ├── blue.html
```

In the `index.html` file, if we wanted to link to, Wikipedia, we would use the full URL to link to it, `<a href="http://www.wikipedia.org">Wikipedia</a>`, as we did above. However, let's say we want to link to red.html in the colors folder. Here we don't need the entire URL; we can use a **relative** path to the resource. The path would simply be `colors/red.html`. Thus, the full syntax looks like:

```html
Here is a link to the <a href="colors/red.html">Red</a> page
```

In this way, you can set up a web page using all relative links and then if, by some chance, you have to migrate your website, you can just plop it down on another server without having to change every link in a web page that could be dozens or hundreds of pages.

There is also a way to link to files in other folders. For example, let's say you want to link to the `panda.jpg` file in `blue.html`. The syntax would look like this: `../images/panda.jpg`. The `../` part tells the browser to go back up one directory, then the rest of the path leads into the `images` folder and finally to the image file. It looks like this:

```html
Check out this picture of a <a href="../images/panda.jpg">panda</a>.
```

Links are one of your most important tools. Use them often. There are other ways to augment the anchor tag, but this is plenty to be getting on with for now.

<!-- Links -->
[this book]: lists.md
[Google]: http://www.google.com
[Wikipedia]: https://www.wikipedia.org/

<!-- images -->
[9]: images/9.png
