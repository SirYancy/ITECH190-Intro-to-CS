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
