# 201 Course 

![web developer](http://coderoo.com.au/blog/wp-content/uploads/2018/02/web.jpg)

----

| number      | subject |
| ----------- | ----------- |
| 1   |Understanding The Problem Domain Is The Hardest Part Of Programming|
| 2   |Chapter 3: “Object Literals” (pp.100-105)|
| 3   |Chapter 5: “Document Object Model” (pp.183-242)|

----

**What is the hardest thing about writing code?**

 > There are many common answers to this question:

* Learning a new technology
* Naming things
* Testing your code
* Debugging
* Fixing bugs
* Making software maintainable
* The list goes on and on.

> A familiar problem
In a good portion of my Pluralsight courses I show the viewer how to build the “Protein Tracker” application.
I am often asked why I keep demonstrating how to build the same simple application over and over again in each of my courses.

> The answer is “familiarity.”

When I first started using the Protein Tracker example in my Android course, I was just looking for a simple example of an application that could be easily understood and implemented.

> The idea behind the Protein Tracker application is that it allows a user to set a goal for the amount of protein to consume in a day.  The user can add protein amounts which are added to a total protein count that is tracked for that user.

**Chapter 3: “Object Literals” (pp.100-105)**

* Height & Width
of Images

> You will also often see an <img>
element use two other attributes
that specify its size:
height
This specifies the height of the
image in pixels.
width
This specifies the width of the
image in pixels.
Images often take longer to
load than the HTML code that
makes up the rest of the page.
It is, therefore, a good idea to
specify the size of the image
so that the browser can render
the rest of the text on the page
while leaving the right amount of
space for the image that is still
loading.
The size of images is increasingly
being specified using CSS rather
than HTML — see pages 409-
410 for more information about
this.

```html
<img src="images/quokka.jpg" alt="A family of
quokka" width="600" height="450" />
```

* Where to Place Images
in Your Code

> Where an image is placed
in the code will affect how it
is displayed. Here are three
examples of image placement
that produce different results:
1: before a paragraph
The paragraph starts on a new
line after the image.
2: inside the start of a
paragraph
The first row of text aligns with
the bottom of the image.
3: in the middle of a
paragraph
The image is placed between the
words of the paragraph that it
appears in.

```html 
<img src="images/bird.gif" alt="Bird" width="100"
height="100" />
<p>There are around 10,000 living species of birds
that inhabit different ecosystems from the
Arctic to the Antarctic. Many species undertake
long distance annual migrations, and many more
perform shorter irregular journeys.</p>
<hr />
<p><img src="images/bird.gif" alt="Bird" width="100"
height="100" />There are around 10,000 living
species of birds that inhabit different
ecosystems from the Arctic to the Antarctic. Many
species undertake long distance annual
migrations, and many more perform shorter
irregular journeys.</p>
<hr />
<p>There are around 10,000 living species of birds
that inhabit different ecosystems from the
Arctic to the Antarctic.<img
src="images/bird.gif" alt="Bird" width="100"
height="100" />Many species undertake long
distance annual migrations, and many more perform
shorter irregular journeys.</p>
```

-----

**Chapter 5: “Document Object Model” (pp.183-242)**

* ID Attribute

> Every HTML element can carry
the id attribute. It is used to
uniquely identify that element
from other elements on the
page. Its value should start with
a letter or an underscore (not a
number or any other character).
It is important that no two
elements on the same page
have the same value for their id
attributes (otherwise the value is
no longer unique).
As you will see when you
come to look at CSS in the next
section, giving an element a
unique identity allows you to
style it differently than any other
instance of the same element
on the page. For example,
you might want to assign one
paragraph within the page
(perhaps a paragraph containing
a pull quote) a different style
than all of the other paragraphs.
In the example on the right, the
paragraph with the id attribute
whose value is pullquote is
made uppercase using CSS.
If you go on to learn about
JavaScript (a language that
allows you to add interactivity to
your pages), id attributes can be
used to allow the script to work
with that particular element.
The id attribute is known as a
global attribute because it can
be used on any element.

```html
<p>Water and air. So very commonplace are these
substances, they hardly attract attention - and
yet they vouchsafe our very existence.</p>
<p id="pullquote">Every time I view the sea I feel
a calming sense of security, as if visiting my
ancestral home; I embark on a voyage of seeing.
</p>
<p>Mystery of mysteries, water and air are right
there before us in the sea.</p>
```

* Class Attribute

> Every HTML element can
also carry a class attribute.
Sometimes, rather than uniquely
identifying one element within
a document, you will want a
way to identify several elements
as being different from the
other elements on the page.
For example, you might have
some paragraphs of text that
contain information that is more
important than others and want
to distinguish these elements, or
you might want to differentiate
between links that point to other
pages on your own site and links
that point to external sites.
To do this you can use the
class attribute. Its value
should describe the class it
belongs to. In the example on
the left, key paragraphs have a
class attribute whose value is
important.
The class attribute on any
element can share the same
value. So, in this example, the
value of important could be
used on headings and links, too.

```html
<p class="important">For a one-year period from
November 2010, the Marugame Genichiro-Inokuma
Museum of Contemporary Art (MIMOCA) will host a
cycle of four Hiroshi Sugimoto exhibitions.</p>
<p>Each will showcase works by the artist
thematically contextualized under the headings
"Science," "Architecture," "History" and
"Religion" so as to present a comprehensive
panorama of the artist's oeuvre.</p>
<p class="important admittance">Hours: 10:00 – 18:00
(No admittance after 17:30)</p>
```

* Block Elemnts

> Some elements will always
appear to start on a new line in
the browser window. These are
known as block level elements.

```html
<h1>Hiroshi Sugimoto</h1>
<p>The dates for the ORIGIN OF ART exhibition are as
follows:</p>
<ul>
<li>Science: 21 Nov - 20 Feb 2010/11</li>
<li>Architecture: 6 Mar - 15 May 2011</li>
<li>History: 29 May - 21 Aug 2011</li>
<li>Religion: 28 Aug - 6 Nov 2011</li>
</ul>
```

* Inline Elements

> Some elements will always
appear to continue on the
same line as their neighbouring
elements. These are known as
inline elements



```html
Timed to a single revolution of the planet around
the sun at a 23.4 degrees tilt that plays out the
rhythm of the seasons, this <em>Origins of Art</em>
cycle is organized around four themes: <b>science,
architecture, history</b> and <b>religion</b>.
```

* Grouping Te xt &
Eleme nts In a Block

> < div> block-elements.html HTML
The < div> element allows you to
group a set of elements together
in one block-level box.
For example, you might create
a < div> element to contain all
of the elements for the header
of your site (the logo and the
navigation), or you might create
a < div> element to contain
comments from visitors.
In a browser, the contents of
the < div> element will start on
a new line, but other than this
it will make no difference to the
presentation of the page.
Using an id or class attribute
on the < div> element, however,
means that you can create
CSS style rules to indicate how
much space the < div> element
should occupy on the screen and
change the appearance of all the
elements contained within it.
It can also make it easier to
follow your code if you have used
< div> elements to hold each
section of the page.

```html
<div id="header">
<img src="images/logo.gif" alt="Anish Kapoor" />
<ul>
<li><a href="index.html">Home</a></li>
<li><a href="biography.html">Biography</a></li>
<li><a href="works.html">Works</a></li>
<li><a href="contact.html">Contact</a></li>
</ul>
</div><!-- end of header -->
```
* Grouping Te xt &
Eleme nts Inline

> < span>
The < span> element acts like
an inline equivalent of the < div>
element. It is used to either:
1. Contain a section of text
where there is no other suitable
element to differentiate it from
its surrounding text
2. Contain a number of inline
elements
The most common reason why
people use < span> elements
is so that they can control the
appearance of the content of
these elements using CSS.
You will usually see that a class
or id attribute is used with
< span> elements:
To explain the purpose of this
< span> element
So that CSS styles can be
applied to elements that
have specific values for these
attributes

```html
<p>Anish Kapoor won the Turner Prize in 1991 and
exhibited at the <span class="gallery">Tate
Modern</span> gallery in London in 2003.</p>
```

* < iframe>

> An iframe is like a little window
that has been cut into your
page — and in that window you
can see another page. The term
iframe is an abbreviation of inline
frame.
One common use of iframes
(that you may have seen on
various websites) is to embed
a Google Map into a page. The
content of the iframe can be any
html page (either located on the
same server or anywhere else on
the web).
An iframe is created using the
< iframe> element. There are a
few attributes that you will need
to know to use it:
src
The src attribute specifies the
URL of the page to show in the
frame.
height
The height attribute specifies
the height of the iframe in pixels.
width
The width attribute specifies
the width of the iframe in pixels.

```html
<iframe
width="450"
height="350"
src="http://maps.google.co.uk/maps?q=moma+new+york
&amp;output=embed">
</iframe>
```

* Summary

* DOCTYPES tell browsers which version of HTML you
are using.
* You can add comments to your code between the
< !-- and -- > markers.
* The id and class attributes allow you to identify
particular elements.
* The <div> and <span> elements allow you to group
block-level and inline elements together.
* <iframes> cut windows into your web pages through
which other pages can be displayed.
* The <meta> tag allows you to supply all kinds of
information about your web page.
* Escape characters are used to include special
characters in your pages such as <, >, and ©.

----

* Adding Video
to Your Pages

> < video>
The < video> element has a
number of attributes which allow
you to control video playback:
src
This attribute specifies the path
to the video. (The example video
is in H264 format so it will only
work in IE and Safari.)
poster
This attribute allows you to
specify an image to show while
the video is downloading or until
the user tells the video to play.

```html
<!DOCTYPE html>
<html>
<head>
<title>Adding HTML5 Video</title>
</head>
<body>
<video src="video/puppy.mp4"
poster="images/puppy.jpg"
width="400" height="300"
preload
controls
loop>
<p>A video of a puppy playing in the snow</p>
</video>
</body>
</html>
```

* summary

* Flash allows you to add animations, v XX ideo and audio to
the web.
* Flash is not supported on iPhone or iPad.
* HTML5 introduces new < video> and < audio>
elements for adding video and audio to web pages, but
these are only supported in the latest browsers.
* Browsers that support the HTML5 elements do not
all support the same video and audio formats, so you
need to supply your files in different formats to ensure
that everyone can see/hear them.

* CSS treats each HTML 
* lement as if it appears inside
* its own box and uses rules to indicate how that
element should look.
* Rules are made up of selectors (that specify the
elements the rule applies to) and declarations (that
indicate what these elements should look like).
* Different types of selectors allow you to target your
rules at different elements.
* Declarations are made up of two parts: the properties
of the element that you want to change, and the values
of those properties. For example, the font-family
property sets the choice of font, and the value arial
specifies Arial as the preferred typeface.
* CSS rules usually appear in a separate document,
although they may appear within an HTML page.

------

@AnasAhmad
