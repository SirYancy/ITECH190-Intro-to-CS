# Tables - The web-dev's secret weapon

Tables are an absolutely essential tool in the Web developer's toolkit. Tables give us a powerful way of structuring information and page content.

There are a set of basic tags that all work together to build the table's structure. Again, the parts of a table are **semantically** defined, so if it looks super confusing one of two things happened: you haven't studied them quite long enough, or the developer that wrote that table did a sloppy job of it and you can curse his or her name forever.  Let's look at the basic tags

| Tag | Description |
|:----|:------------|
|`<table>`| Defines a table. The outermose tag. |
|`<tr>`| Defines a table row. Must be inside of a `<table>` tag |
|`<td>`| Defines a table data cell. Must be inside a `<tr>` tag |
|`<th>`| Defines a table header cell. Must be inside a `<tr>` and is only stylistically different from `<td>` |

These four tags (and a couple of their **attributes**) give us practically infinite structure possibilities in web content. Let's see it in action:

```html

    <table>
        <tr>
            <td><img src="STEM-logo.jpg" width="100px" alt="STEM Logo" /></td>
            <td>Introduction to Computer Science</td>
        </tr>
    </table>

    <table>
        <tr>
            <th>Name:</th>
            <td>Eric Kuha</td>
        </tr>
        <tr>
            <th>Age:</th>
            <td>36</td>
        </tr>
        <tr>
            <th>Hometown:</th>
            <td>Bemidji, MN</td>
        </tr>
        <tr>
            <th>Major:</th>
            <td>Computer Science</td>
        </tr>
    </table>
```

![11]

In this example, there are two tables. The first table has one `<tr>` element. Often tables are used to more easily format the structure of certain page elements, such as, in this case, a header with a logo. By inserting the logo into the header with a title in the next table cell over, you can simplify the process of building a nicely designed page heading. The second table is an informational table. Notice the difference between the `<th>` and the `<td>` tags. `<th>` will, in most browsers, make the text bold and center it within its cell whereas `<td>` will usually just display the text with minimal styling.

## Table Styling

Tables can be styled using many of the same methods that you can style other HTML elements. Like an image, you can set the table's height and width (most often just width) by adding `width="50%"` attribute to to the `<table>` opening tag.

There used to be a table border attribute that you could apply, but it is no longer technically supported in HTML5. Instead, to add table borders (and other styling) it is generally preferable to use CSS styling which we will look at in the next section.

## Tables in practice

If you find yourself doing any web development at all, being able to format text and data in a tabular format will become critical. Remember, tables are not just tabular data, though. They are often just a great way to format page elements.

<!-- Images -->
[11]: images/11.png
