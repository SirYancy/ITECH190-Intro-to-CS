# HTML and CSS - Literally made for each other

We have talked a lot about using HTML _semantically_. What this means is that we define HTML elements by what they _mean_ rather than how they will _look_. But that doesn't mean that we are giving up control over how the web browser should display your content. For example, by default, a `<table>` has not lines. But it is _very_ common to want some sort of graphical lines separating the cells of your tables. So, while HTML gives your content a kind of skeleton, for the styling, we refer to another web language called *Cascading Stylesheets* or *CSS*.

# CSS Basics

The simplest way to use CSS to style our web pages is to use what's called an "inline style" attribute. Like the `width` attribute, the `style` attribute goes inside of the opening tag of an element. Thus, if you wanted to add some particular style to a paragraph of text, for instance, the code might look like this:

```html
<p style="[Define Some Style]">My paragraph</p>
```

Like any other attribute, you define it with the word "style", followed by an equal sign (=), and then define your styles inside of a double quotes ("). But what do these styles look like?  When you're adding inline CSS styling, the style consists of two parts: the *property* and the *value*. So, if I wanted to change the background color of an element (yes, you can do this with _any_ element), then my inline attribute would look like this:

```html
<h1 style="background-color:Red">A red heading</h1>
<p style="background-color:DarkBlue">My Blue Paragraph</p>
```
![12]

Likewise, you can change the text color as well by adding the *color* style:

```html
<h1 style="background-color:Red;color:white;">A red heading</h1>
<p style="background-color:DarkBlue;color:white">My Blue Paragraph</p>
```
![13]


<!-- Images -->
[12]: images/12.png
[13]: images/13.png
