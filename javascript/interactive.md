# Interactivity

## Terminology

<dl>
    <dt>Concatenation</dt>
    <dd>Combining two strings of text into a single string of text.</dd>
    <dt>Escape Sequence</dt>
    <dd>A character used to inform a code interpreter or compiler that other characters normally reserved for syntax are actually content.</dd>
</dl>
## Handling User Input

Computers would be pretty useless if they did not respond to user input. An online store, for example, needs be able to handle all sorts of input. They need to be able to move between product pages for one, but they also need to accept form data like a user's address and credit card information in order to process payments and shipping. There's a lot that goes on behind the scenes on a website's backend, like database queries and the like, but this lesson covers some of the basic JS frontend interactivity that you can use and shows how HTML and JavaScript can be used to make a web page behave in interesting ways.

## Example 1: Press this Button

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Do Not Press</title>
</head>
<body>
    <p>
    This page does nothing.
    </p>
    <input type="button" value="Do not click here."
                         onclick="
                         document.getElementById('output').innerHTML=
                         '<p>Do <em>not</em> click it again.</p>';
                         "/>
    <div id="output"></div>
</body>
</html>
```

You can find a working version of this example [here](http://itech190.erickuha.com/interactive_js/do_not_press.html).

The first thing to look at here is the button's **onclick** attribute. It has a single line of JS code (broken into two lines for readability reasons) that searches for an element with the id "output" and assigns a new value to its `innerHTML`. The JS `innerHTML` variable references the information *between* two HTML tags. Assigning a value to it directly like this replaces all content between the two tags. In this case, it's a simple `<div>` tag. Remember, `<div>` tags don't actually do much except give you a place to apply formatting create logical structure.

The page has an empty pair of div tags with the id "output". So, the button's **onclick** attribute will insert content between the two div dags causing them to appear in the page.

Lastly, look at the string that we're assigning to the tags: `<p>Do <em>not</em> click it again.</p>`. This is just a little bit of HTML, a `<p>` tag with a little formatting in the middle. It is important to remember that JS doesn't recognize any of this as HTML. It just sees a string of text. It isn't until it's inserted into the `<div>` element and then parsed by the web browser that it is interpreted as HTML. To re-iterate, as far as JS is concerned, it's just a string of characters and nothing more. This is actually a very useful and powerful feature, but it does require some attention to detail to get it right as we shall see in subsequent examples.

## Example 2: Welcome Page

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title></title>
</head>
<body>
    <h2>Greetings</h2>
    <p>
    What is your name? <input type="text" id="namebox" size=12 value="" />
    </p>
    <input type="button" value="Click"
                         onclick="document.getElementById('output').innerHTML=
                         '<p>Welcome ' + document.getElementById('namebox').value +
                         '. So glad you could come.</p>';"/>
    <hr />
    <div id="output"></div>
</body>
</html>
```

In this simple example, the *onclick* attribute again contains only a single line of JS script that takes the contents of a text box and inserts whatever it finds there into a string of text that again is outputted to a div at the bottom of the page.

Pay attention to the way the addition operator (+) is used to combine strings. This is called *concatenation*. Look very carefully about how this concatenation is used to define a `<p>` tag and where the period is used to end a sentence. These are little details that are often overlooked by new programmers but soon become second nature.

## Example 3: Event Scheduler

```html
<!DOCTYPE html>
<html>
<head>
	<title>Form Demonstration</title>
</head>
<body>
	<h2>Event Scheduler</h2>
	<p>
		What's your name:
		<input type="text" id="nameBox" size="20" value="Fred" /> <br />
		What do you want to do:
		<input type="text" id="activityBox" size="20" value="birthday" /> <br />
		Enter a date:
		<input type="date" id="dateBox" size="20" value="" /> <br />
	</p>
	<input type="button" value="Click to schedule"
		onclick="
            name = document.getElementById('nameBox').value;
            activity = document.getElementById('activityBox').value;
            date = document.getElementById('dateBox').value;

            document.getElementById('output').innerHTML=
                '<p>Hello, ' + name +
			    ',</p> <p>I am really excited to attend your ' +
			    activity + ' on ' + date +
                '. It sounds like fun!</p><br />' + 
                '<p style=\'text-align:right\'>Regards,<br>Eric</p>';"
                
    />


	<div id="output"></div>
</body>
</html>
```

There's a lot going on here, and you're going to need it for the lab. Duplicate (re-type, don't just copy and paste) the code into a new html file. Run it and see what it does. The working example can be found [here](http://itech190.erickuha.com/interactive_js/form.html).

The most daunting part of this example isn't what it does, but rather some of the fiddly syntax. Let's go through it.

First, there are three inputs, all with unique **id** attributes. Note that the first two are **type** text and the last one has **type** date. This works basically like a textbox except that it informs the web browser to create a date-picker widget for convenience.

In the button's **onclick** attribute, the code is broken into several lines and is formatted for easier reading. The first three lines of code grab the values from the first three inputs and store them in variables for later use. The variable names can be anything, but it's good practice to use variable names that mean something.  The last line of code is actually fairly straightforward, but might take a couple of minutes of study to see everything that's going on. First, it's assigning some content to the **innerHTML** attribute of our "output" div. The string that it's inserting is concatenated from several sub-strings. Looking carefully at this code, we can see the the string is constructed into a bit of HTML code using the variables that were captured from the input boxes.

Assuming the name "Fred", the activity "birthday", and the date "2017-6-10", the string constructed would look like this:

`'<p>Hello, Fred,</p> <p>I am really excited to attend your birthday on 2017-6-10.'
'It sounds like fun!</p><br /><p style='text-align:right'>Regards,<br>Eric</p>'`

Formatted for easier reading, it would look like this:

```html
<p>Hello, Fred,</p>
<p>I am really excited to attend your birthday on 2017-6-10. It sounds like fun!</p>
<br />
<p style='text-align:right'>
    Regards,
    <br>
    Eric
</p>'
```

Sometimes, when you want to construct a complex string like this, it's better to start with the end product and work backwards to get to the JS code that will produce it. **Also,** note that in the code, there are some backslashes (\) in the last line of code that are not there once it's converted to HTML. These are called **escape sequences** **escapes**. Since the single quote right after the `<p style=` needs to be there for the HTML code, but would be interpreted by JS as the end of a string, JS uses the backslash to "escape" it, letting JS know that those single quotes are part of the string.

In the next section, we will expand on user interaction in JS and HTML.
