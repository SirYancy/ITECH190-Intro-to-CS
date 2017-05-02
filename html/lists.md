# HTML Lists

People love lists. We love to list things because they are great ways to show information. Top movies of all time. Greatest baseball players of all time. Things I want to buy when I go to the grocery store. The list goes on.

Since a list is such a semantically important aspect of written language, HTML has list tags built in. They come in two varieties.

## The List Tags

| Tag | Purpose |
| --- | --- |
|`<ol>`|Defines an ordered list|
|`<ul>`|Defines an unordered list|
|`<li>`|Defines a list item|

There are two types of lists as far as HTML is concerned. Ordered lists and unordered lists. An ordered list is defined by the `<ol>` tag and by default creates a numbered list. Likewise, the unordered list is defined by the `<ul>` tag and creates a bulleted list. Both of these lists can be styled to display differently. For example, an ordered list can display letters instead of numbers and a bullet list can show tiny squares instead of tiny circles.

No matter which type of list you use, to define an item, you just stick it inside a pair of `<li>` tags. Thus, the following is possible:

```html
<h3>My Favorite Movies</h3>
<ul>
    <li><em>Big Trouble in Little China</em></li>
    <li><em>Starship Troopers</em></li>
    <li><em>Groundhog Day</em></li>
    <li><em>Yojimbo</em></li>
    <li><em>Glengarry Glen Ross</em></li>
</ul>
```

Will render like so:

![7]

Notice the `<em>` tags that were used to italicize the text. Since it is inside the `<li>` tag, it _must_ be closed before the `</li>` tag. Tags work their way from the inside out. It is important to note, however, breaking many of these rules (like closing tags from the inside out) will not necessarily cause your page not to load or render. The page will still render. It will still display. And often, it will not even have any visible errors. The problem with breaking the syntax rules is that its behavior will be _unpredictable_. You can't know exactly how it's going to behave if you don't obey the rules. And even if it looks fine in one browser, there's no guarantee that it's going to look the same in another browser. So. Follow the rules.

## Nesting Lists

You can nest lists inside of each other to create sub-lists by simply defining a new list inside of a `<li>` tag pair. For example,

```html
<h3>My Favorite Fruits</h3>
<ul>
    <li>Kiwi</li>
    <li>Apple
        <ul>
            <li>Braeburn</li>
            <li>Honeycrisp</li>
            <li>Fuji</li>
        </ul>
    </li>
    <li>Orange</li>
</ul>
```

Pay close attention to how the lists are defined and where they are closed. This renders like this:
![8]

Observe how the list bullets are different in the nested list. Lists are one of your most important tools in web design. They are used practically everywhere and give you a nice, uncomplicated way to semantically define collections of ideas, objects, and ideas.

<!-- images -->
[7]: images/7.png
[8]: images/8.png
