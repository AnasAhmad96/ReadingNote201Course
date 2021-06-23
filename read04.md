# 201 Course 

![web developer](http://coderoo.com.au/blog/wp-content/uploads/2018/02/web.jpg)

----

| number      | subject |
| ----------- | ----------- |
| 1   |Ch.4 “Links” (pp.74-93)|
| 2   |Chapter 15: “Layout” (pp.358-404)|
| 3   |Chapter 3 (first part): “Functions, Methods, and Objects” (pp.86-99 ONLY)|
| 4   |Article: “6 Reasons for Pair Programming”|

----

1- **Ch.4 “Links” (pp.74-93)**

* Writing Links

> Links are created using the <a> element. Users can click on anything
between the opening <a> tag and the closing </a> tag. You specify
which page you want to link to using the href attribute.
>>< a href="http://www.imdb.com">IMDB</a>

* Linking to Other Sites

> < a> other-sites.html HTML
Links are created using the < a>
element which has an attribute
called href. The value of the
href attribute is the page that
you want people to go to when
they click on the link.
Users can click on anything that
appears between the opening
< a> tag and the closing < /a>
tag and will be taken to the page
specified in the href attribute.
When you link to a different
website, the value of the href
attribute will be the full web
address for the site, which is
known as an absolute URL.

```html
<p>Movie Reviews:
<ul>
<li><a href="http://www.empireonline.com">
Empire</a></li>
<li><a href="http://www.metacritic.com">
Metacritic</a></li>
<li><a href="http://www.rottentomatoes.com">
Rotten Tomatoes</a></li>
<li><a href="http://www.variety.com">
Variety</a></li>
</ul>
</p>
```

* Linking to Other Pages
on the Sa me Site

> < a>
When you are linking to other
pages within the same site,
you do not need to specify the
domain name in the URL. You
can use a shorthand known as a
relative URL.
If all the pages of the site are in
the same folder, then the value
of the href attribute is just the
name of the file.
If you have different pages of a
site in different folders, then you
can use a slightly more complex
syntax to indicate where the
page is in relation to the current
page. You will learn more about
these on the pages 81-84.
If you look at the download
code for each chapter, you will
see that the index.html file
contains links that use relative
URLs.

```html 
<p>
<ul>
<li><a href="index.html">Home</a></li>
<li><a href="about-us.html">About</a></li>
<li><a href="movies.html">Movies</a></li>
<li><a href="contact.html">Contact</a></li>
</ul>
</p>
```

* Email Links

> mailto: email-links.html HTML
To create a link that starts up
the user's email program and
addresses an email to a specified
email address, you use the < a>
element. However, this time the
value of the href attribute starts
with mailto: and is followed by
the email address you want the
email to be sent to.
On the right you can see that
an email link looks just like any
other link but, when it is clicked
on, the user's email program
will open a new email message
and address it to the person
specified in the link.

```html
<a href="mailto:jon@example.org">Email Jon</a>
```

* Op ening Links in
a New Window

> target
If you want a link to open in a
new window, you can use the
target attribute on the opening
< a> tag. The value of this
attribute should be _blank.
One of the most common
reasons a web page author
might want a link to be opened
in a new window is if it points to
another website. In such cases,
they hope the user will return
to the window containing their
site after finishing looking at the
other one.
Generally you should avoid
opening links in a new window,
but if you do, it is considered
good practice to inform users
that the link will open a new
window before they click on it.

```html 
<a href="http://www.imdb.com" target="_blank">
Internet Movie Database</a> (opens in new window)
```

* Summary

Links are created using the < a> element.
* The < a> element uses the href attribute to indicate
the page you are linking to.
* If you are linking to a page within your own site, it is
best to use relative links rather than qualified URLs.
* You can create links to open email programs with an
email address in the "to" field.
* You can use the id attribute to target elements within
a page that can be linked to.

-----

2- **Chapter 15: “Layout” (pp.358-404)**

* Relative Positioning
position:relative

> Relative positioning moves an
element in relation to where it
would have been in normal flow.
For example, you can move it 10
pixels lower than it would have
been in normal flow or 20% to
the right.
You can indicate that an element
should be relatively positioned
using the position property
with a value of relative.
You then use the offset
properties (top or bottom and
left or right) to indicate how
far to move the element from
where it would have been in
normal flow.
To move the box up or down,
you can use either the top or
bottom properties.
To move the box horizontally,
you can use either the left or
right properties.
The values of the box offset
properties are usually given in
pixels, percentages or ems.

```html
<body>
<h1>The Evolution of the Bicycle</h1>
<p>In 1817 Baron von Drais invented a walking
machine that would help him get around the
royal gardens faster...</p>
</body>
```

* Absolute Positioning 
position:absolute

> When the position property
is given a value of absolute,
the box is taken out of normal
flow and no longer affects the
position of other elements on
the page. (They act like it is not
there.)
The box offset properties (top
or bottom and left or right)
specify where the element
should appear in relation to its
containing element.
In this example, the heading has
been positioned at the top of the
page and 500 pixels from its left
edge. The width of the heading is
set to be 250 pixels wide.
The width property has
also been applied to the <p>
elements in this example
to prevent the text from
overlapping and becoming
unreadable.

``` html
<body>
<h1>The Evolution of the Bicycle</h1>
<p>In 1817 Baron von Drais invented a walking
machine that would help him get around the
royal gardens faster...</p>
</body>
```

```css
h1 {
position: absolute;
top: 0px;
left: 500px;
width: 250px;}
p {
width: 450px;}
```

* Fixed Positioning
position:fixed 

> Fixed positioning is a type
of absolute positioning that
requires the position property
to have a value of fixed.
It positions the element in
relation to the browser window.
Therefore, when a user scrolls
down the page, it stays in the
exact same place. It is a good
idea to try this example in your
browser to see the effect.
To control where the fixed
position box appears in relation
to the browser window, the box
offset properties are used.
In this example, the heading
has been positioned to the top
left hand corner of the browser
window. When the user scrolls
down the page, the paragraphs
disappear behind the heading.
The < p> elements are in normal
flow and ignore the space that
the < h1> element would have
taken up. Therefore, the
margin-top property has
been used to push the first < p>
element below where the fixed
position < h1> element is sitting.

```css
h1 {
position: fixed;
top: 0px;
left: 50px;
padding: 10px;
margin: 0px;
width: 100%;
background-color: #efefef;}
p.example {
margin-top: 100px;}
```

* Overlapping El ements
z-index

> When you use relative, fixed, or
absolute positioning, boxes can
overlap. If boxes do overlap, the
elements that appear later in the
HTML code sit on top of those
that are earlier in the page.
If you want to control which
element sits on top, you can use
the z-index property. Its value
is a number, and the higher the
number the closer that element
is to the front. For example, an
element with a z-index of 10
will appear over the top of one
with a z-index of 5.
This example looks similar to
the one on page 368, but it
uses relative positioning for
the < p> elements. Because
the paragraphs are relatively
positioned, by default they
would appear over the top of the
heading as the user scrolls down
the page. To ensure that the
< h1> element stays on top, we
use the z-index property on the
rule for the < h1> element.
The z-index is sometimes
referred to as the stacking
context (as if the blocks have
been stacked on top of each
other on a z axis). If you are
familiar with desktop publishing
packages, it is the equivalent
of using the 'bring to front' and
'send to back' features.

```css
h1 {
position: fixed;
top: 0px;
left: 0px;
margin: 0px;
padding: 10px;
width: 100%;
background-color: #efefef;
z-index: 10;}
p {
position: relative;
top: 70px;
left: 70px;}
```

* Fl oating El ements
float 

> The float property allows you
to take an element in normal
flow and place it as far to the
left or right of the containing
element as possible.
Anything else that sits inside
the containing element will
flow around the element that is
floated.
When you use the float
property, you should also use the
width property to indicate how
wide the floated element should
be. If you do not, results can be
inconsistent but the box is likely
to take up the full width of the
containing element (just like it
would in normal flow).
In this example, a
< blockquote> element is
used to hold a quotation. It's
containing element is the
< body> element.
The < blockquote> element
is floated to the right, and the
paragraphs that follow the quote
flow around the floated element.

```css
blockquote {
float: right;
width: 275px;
font-size: 130%;
font-style: italic;
font-family: Georgia, Times, serif;
margin: 0px 0px 10px 10px;
padding: 10px;
border-top: 1px solid #665544;
border-bottom: 1px solid #665544;}
```

* El ements Side-by-Side

> A lot of layouts place boxes
next to each other. The float
property is commonly used to
achieve this.
When elements are floated, the
height of the boxes can affect
where the following elements sit.
In this example, you can see six
paragraphs, each of which has a
width and a float property set.
The fourth paragraph does not
go across to the left hand edge
of the page as one might expect.
Rather it sits right under the
third paragraph.
The reason for this is that the
fourth paragraph has space to
start under the third paragraph,
but it cannot go any further to
the left because the second
paragraph is in the way.
Setting the height of the
paragraphs to be the same
height as the tallest paragraph
would solve this issue, but it
is rarely suited to real world
designs where the amount of
text in a paragraph or column
may vary. It is more common
to use the clear property
(discussed on the next page) to
solve this issue.

```css
body {
width: 750px;
font-family: Arial, Verdana, sans-serif;
color: #665544;}
p {
width: 230px;
float: left;
margin: 5px;
padding: 5px;
background-color: #efefef;}
```

* Multiple Style Sheets
link 

> On this page you can see the
other technique for including
multiple style sheets. Inside the
< head> element is a separate
< link> element for each style
sheet.
The contents of site.css are
identical to styles.css on the
left hand page, except the code
does not contain @import rules.
As with all style sheets, if two
rules apply to the same element
then rules that appear later in a
document will take precedence
over previous rules.
In the example on this page,
any rules in typography.css
would take precedence over
rules in site.css (because the
typography rules are included
after the other rules).
In the example on the previous
page, the rules in styles.css
would take precedence over the
rules in typography.css. This
is because when the @import
rule is used, that is the point at
which the browser considers the
rules live.

```html
<!DOCTYPE html>
<html>
<head>
<title>Multiple Style Sheets - Link</title>
<link rel="stylesheet" type="text/css"
href="css/site.css" />
<link rel="stylesheet" type="text/css"
href="css/tables.css" />
<link rel="stylesheet" type="text/css"
href="css/typography.css" />
</head>
<body>
<!-- HTML page content here -->
</body>
</html>
```

* Summary
* < div> elements are often used as containing elements
to group together sections of a page.
* Browsers display pages in normal flow unless you
specify relative, absolute, or fixed positioning.
* The float property moves content to the left or right
of the page and can be used to create multi-column
layouts. (Floated items require a defined width.)
* Pages can be fixed width or liquid (stretchy) layouts.
* Designers keep pages within 960-1000 pixels wide,
and indicate what the site is about within the top 600
pixels (to demonstrate its relevance without scrolling).
* Grids help create professional and flexible designs.
* CSS Frameworks provide rules for common tasks.
* You can include multiple CSS files in one page

---- 

3- **Ch.4 “Links” (pp.74-93)**

* Summary 

* A script is made up of a series of statements. Each
statement is like a step in a recipe.
* Scripts contain very precise instructions. For example,
you might specify that a value must be remembered
before creating a calculation using that value.
* Variables are used to temporarily store pieces of
information used in the script.
* Arrays are special types of variables that store more
than one piece of related information.
* JavaScript distinguishes between numbers (0-9),
strings (text), and Boolean values (true or false).
* Expressions evaluate into a single value.
* Expressions rely on operators to calculate a value.
* A script is made up of a series of statements. Each
statement is like a step in a recipe.
* Scripts contain very precise instructions. For example,
you might specify that a value must be remembered
before creating a calculation using that value.
* Variables are used to temporarily store pieces of
information used in the script.
* Arrays are special types of variables that store more
than one piece of related information.
* JavaScript distinguishes between numbers (0-9),
strings (text), and Boolean values (true or false).
* Expressions evaluate into a single value.
* Expressions rely on operators to calculate a value.


**Declaring Function**

```js
function nameoffunction () {
    what do you want do
}
```

**Calling functions**

```js
nameoffunction ();
```

-----

3- **Article: “6 Reasons for Pair Programming”**

*6 Reasons for Pair Programming*

* How does pair programming work?
> While there are many different styles, pair programming commonly involves two roles: the Driver and the Navigator. The Driver is the programmer who is typing and the only one whose hands are on the keyboard. Handling the “mechanics” of coding, the Driver manages the text editor, switching files, version control, and—of course writing—code. The Navigator uses their words to guide the Driver but does not provide any direct input to the computer. The Navigator thinks about the big picture, what comes next, how an algorithm might be converted in to code, while scanning for typos or bugs. The Navigator might also utilize their computer as a second screen to look up solutions and documentation, but should not be writing any code.

* Why pair program?
> While learning to code, developers likely study several programming languages. Similar to a foreign language class, there are four fundamental skills that help anyone learn a new language: Listening: hearing and interpreting the vocabulary Speaking: using the correct words to communicate an idea Reading: understanding what written language intends to convey Writing: producing from scratch a meaningful
Pair programming touches on all four skills: developers explain out loud what the code should do, listen to others’ guidance, read code that others have written, and write code themselves.

* Learning from fellow students
> Everyone has a different approach to problem solving; working with a teammate can expose developers to techniques they otherwise would not have thought of. If one developer has a unique approach to a specific problem, pair programming exposes the other developer to a new solution.
Often times, the developers in a pairing have different skill sets. If one programmer is more experienced in a certain skill, they can teach a student who is less familiar with that area. The less experienced developer benefits from the experienced developer’s knowledge and guidance, and the latter benefits from explaining the topic in their own words, further solidifying their own understanding.

* Social skills 

> Pair programming is great for improving social skills. When working with someone who has a different coding style, communication is key. This can become more difficult when two programmers have different personalities. Pair programming not only improves programming skills, but can also help programmers develop their interpersonal skills. When just grabbing the keyboard and taking over isn’t an option, getting good at finding the right words is a skill unto itself.
This has long-term career impacts. As much as employers want strong programmers, they know it’s essential to hire people who can work well with others.

* Job interview readiness

> A common step in many interview processes involves pair programming between a current employee and an applicant, either in person or through a shared screen. They will carry out exercises together, such as code challenges, building a project or feature, or debugging an existing code base. By doing so, companies can get a better feel for how an applicant will fit into the team and their collaboration style.
For most roles, the ability to work with and learn from others and stellar communication skills are as (or more!) important to a company than specific technical skills. Pair programming strengthens all of those skills.

* Work environment readiness

> Many companies that utilize pair programing expect to train fresh hires from CS-degree programs on how they operate to actually deliver a product. Code Fellows graduates who are already familiar with how pairing works can hit the ground running at a new job, with one less hurdle to overcome.

----

@AnasAhmad