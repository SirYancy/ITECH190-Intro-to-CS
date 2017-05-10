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

These are called *inline* styles. You can also define styles in a `<style>` tag in the `<head>`, or even in their own stylesheet file. Let's look at both of these here.

# Embedded Stylesheets

One way to make a quick stylesheet for a single web page is to define an embedded stylesheet. It's defined in the `<head>` element of your page. Now, there's a few bits of odd syntax here, but it's not too difficult when you get used to it.

The `<style>` tag gets an attribute `type="text/css"` this is called a mime type and you don't really have to remember that except that it needs to be there. It tells the web browser what kind of stylesheet you're defining (as if there were another kind).

Inside the `<style>` tags, we define styles using the following syntax:

`*selector* { *property*: *value*; }`

The selector is a tag element in your web page like `body` or `p` or `h1`. And the properties are much like like inline styles. You can change the `background-color` by using a value like `blue` or `#3a7ca5` (a hex color value; more on this later). Finally, after you define a style, you must end the line with a semicolon (;). 

There are many, many different styles that can be manipulated like this and CSS has many different ways that you can select exactly the elements you want. But for the purposes of this class, we'll just mess with a few. Let's look at an example:

```html
<!DOCTYPE HTML>
<html>

<head>
	<meta charset="utf-8" />
	<title>Tables</title>

    <style type="text/css">

    body {
        background-color: lightblue;
    }
    
    h1 {
        color: navy;
        margin-left: 20px;
    }

    </style>

</head>

<body>

<h1>
    Koalas  
</h1>
<img src="koala.png" />
<p>
   Koalas are the most dangerous animals in the world. 
</p>


</body>
</html>
```
![14]

In the `<style>` tags we are selecting the `body` element and changing its *background-color* to *lightblue*. Then, we are selecting the `h1` tag and changing its text color to *navy* and giving it a 20 pixel margin on the left. It is important to note that when you select a tag in this way, it applies it to _all_ instances of that tag in the entire document.

## External Stylesheets

Last, let's look at external stylesheets. An external stylesheet is defined in its own file and then linked to the web page so that the browser rendering the page knows where to find it. You define the styles exactly as you would in an embedded stylesheet, only it's not in a `style` tag. 

For example, let's say we have the following stylesheet defined:

```css
h1 {
    text-align: center
   }

table, th, td {
    border: 1px solid black;
    border-collapse: collapse;
    padding: 4px;
}

th {
    text-align: left;
    background-color: rgba(128, 0, 0, 50);
    color: white;
}
```

Notice a couple of things. The selectors can be chained together by separating them with a comma. Observe that we are adding borders and padding to `table`, `th`, and `td`. 

<!-- Images -->
[12]: images/12.png
[13]: images/13.png
[14]: images/14.png
