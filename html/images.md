# Images in Web Pages

One of the most important aspects of hypertext is the ability to share many kinds of media, often even embedded in the same Web Page. There are as many ways of embedding media in a web page as there are types of media. And then some. However, nothing will be quite as ubiquitous as adding an image to your Web page. Let's meet the `<img>` tag.

## The `<img>` tag

The image tag is the first place where we really have to wrestle with the concept of an **attribute**. Anchor tags had the `href` attribute, and there are tons of them in the average page `<head>`, but those are mostly copy-pasted without caring what any of it means. In the `<img>` tag, there are many attributes and each one has many possible settings. So let's start simple.

This example assumes that the image file and the html file are in the same directory. Most standard image formats work just fine, including `.jpg`, `.png`, `.gif`, `.tiff`, etc. so let's assume that we have `profile_pic.jpg` and `profile.html` in the same folder. The following code is in the html file:

```html
    <h1>Welcome to my web page!</h1>
    <img src="profile_pic.jpg" />
    <p>
        Stay as long as you'd like.
    </p>
```
![10]

The `<h1>` and the `<p>` tag should already be familiar to you. The `<img>` tag is a little different

There are two main features that set it apart from most of the tags we've looked at. For one, it closes itself. Notice that, like the line break tab, `<br />` it has a **forward slash** before the right angle bracket. This signifies that the tag closes itself. That is, there is not corresponding `<img></img>` tags. It's just the `<img />` tag.

The next thing that you should observe is the **src** attribute. The **source** attribute tells us where the image is located. The semantic difference between **src** and **href** is subtle but importance. An **src** attribute points to the resource that will _replace_ this element, whereas the **href** attribute establishes a _relationship_ between this element and some other resource. Regardless, the syntax is largely the same and the end result is an image rendered in your web browser.

## `<img>` Attributes

There are actually many attributes that can be applied to an image file. Let's look at a few of the more important ones.

| Attribute | Values | Description |
|:----|:----|:----|
|src | _URL_ | Sets the location for the image resource |
|alt | _Some text_ | sets the alternative text for the image (in case it doesn't load)|
|height | _# of pixels_ | Sets the height of the image |
|width | _# of pixels, percentage_ | Sets the width of the image |

These four attributes are generally regarded as essential. Most standards require that all four be included in any `<img>` tag. So looking at all of them, the **src** attribute is obvious. Without it, you have no image. The **alt** text is also important because it is what displays if the image fails to load (or is taking its time loading) to at least convey _some_ meaning to the reader as the image loads. The **height** and **width** attributes are _technically_ optional, though as a matter of style, it is highly advised that you use them. And, generally, in a static web page, you should set them to their native sizes. This image happens to be 300 pixels by 284 pixels. By these rules, the code snippet for this image _should_ read:

```html
<img src="profile_pic.jpg" width="300" height="284" alt="Profile Picture" />
```

Or at least, this is how you'd do it for a static page with static images. In the days of mobile operating systems and a million different screen sizes and aspect ratios, the need for pages that can resize their own content, so-called **responsive** Web pages, is becoming more important to convincing people to read it. If you've ever looked at a Web page that just doesn't work right on a mobile screen, you have seen a page that does not adhere to **responsive** design principles.

For our part, our main effort at responsiveness in our web pages will be to replace hard-coded pixel sizes into our image tags. Instead, you can use a percentage. The 



<!-- images -->
[10]: images/10.png
