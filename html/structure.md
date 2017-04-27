# Anatomy of an HTML Doucment

The [World Wide Web Consortium] is an international organization currently still lead by Tim Berners-Lee. It maintains the standards for HTML and its companion styling language CSS (which we will cover a little later in this course). The early days of HTML were a bit crazy. Different web browsers might behave very differently and as a result, there was a proliferation of tags that might work in one browser, but not in others. Finally, the W3C was able to get things under control. And now, with HTML5, we have a very structured set of standards and rules that govern the tags and styling that a web browser _must_ adhere to, and what it must avoid. So, let's look at the basic structure of a modern web page.

Let's look at a very rudimentary but well-structured web-page:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>My Title</title>
</head>
<body>
    <h1>Welcome!</h1>
    <p>
        This is my website.
    </p>
</body>
</html>
```

## The DOCTYPE Declaration

The first item on a web document is the DOCTYPE declaration. This tells the web browser what sort of document this is. For all HTML5 documents, the declaration looks like this:

`<!DOCTYPE html>`

That's it. This sets HTML5 apart from older HTML4 or earlier declarations. It's a great because it's nice and clean and not confusing. To contrast, an HTML 4.01 declaration looks like this:

`<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">`

So this is a nice improvement.

## The `<html>` Tag

Directly after the DOCTYPE declaration is the `<html>` tag. This tag informs the browser that everything after it is html code. Everything in the entire web page (other than the DOCTYPE declaration) should be inside the `<html>` tags. Notice the `lang="en"` bit. This is called a tag **attribute**. Attributes are ways of augmenting the functionality of a tag. In this case, the attribute is informing the web browser that this page is written in English. This helps search engines like Google to more accurately index your website.

Often things like this seem like they have no effect. But they do. On the one hand, it's just good practice. But, while they will not necessarily change how your web page renders, they _do_ affect how well it plays with the rest of the Web.

## The `<head>` Tag

After the DOCTYPE declaration, a web page generally has a `<head>` element which is typically where you'll include meta data (character encoding, text language, authorship information, etc) as well as link up CSS stylesheets and scripts. In this case, we have the following two items:

* a `<meta>` tag which informs the browser that the web page is using the [UFT-8] character encoding standard.
* a `<title>` tag which defines the title in the browser tool bar, gives the page a name when you bookmark it, and defines its title for search-engine results. It is required in all web pages.<br>![5]

## The `<body>` Tag

The `<body>` tag semantically defines the portion of your web page that will render in the web browser. It's where you put all of your _content_.

## Putting it All Together

Throughout this course, you will see many different web pages in the demos and will build several of your own. And they are all going to be a little bit different. They may have different elements in the `<head>` tag, for instance. But through it all, a strict adherence to the W3C standards will be observed. If there's a particular element or attribute that you do not understand, feel free to search for it in your search-engine of choice and see what you can find out. Computer Science sometimes forces you to search out information on your own. Excercise your Google-Fu early and often. It's good to learn good habits early.

Despite all of the things going on under the hood, this page renders very simply:

![6]


<!-- Links -->
[World Wide Web Consortium]: https://www.w3.org/
[UTF-8]: https://en.wikipedia.org/wiki/UTF-8

[5]: images/5.png
[6]: images/6.png
