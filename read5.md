# 201 Course 

![web developer](http://coderoo.com.au/blog/wp-content/uploads/2018/02/web.jpg)

----

| number      | subject |
| ----------- | ----------- |
| 1   |Chapter 5: “Images” (pp.94-125)|
| 2   |Chapter 11: “Color” (pp.246-263)|
| 3   |Chapter 12: “Text” (pp.264-299)|

----

1- **Chapter 5: “Images” (pp.94-125)**

* Adding Images

> < img> images.html HTML
To add an image into the page
you need to use an < img>
element. This is an empty
element (which means there is
no closing tag). It must carry the
following two attributes:
src
This tells the browser where
it can find the image file. This
will usually be a relative URL
pointing to an image on your
own site. (Here you can see that
the images are in a child folder
called images — relative URLs
were covered on pages 83-84).
alt
This provides a text description
of the image which describes the
image if you cannot see it.
title
You can also use the title
attribute with the < img> element
to provide additional information
about the image. Most browsers
will display the content of this
attribute in a tootip when the
user hovers over the image.
Adding Images
The text used in the alt attribute
is often referred to as alt text.
It should give an accurate
description of the image content
so it can be understood by
screen reader software (used by
people with visual impairments)
and search engines.
If the image is just to make a
page look more attractive (and
it has no meaning, such as a
graphic dividing line), then the
alt attribute should still be used
but the quotes should be left
empty.

```html 
<img src="images/quokka.jpg" alt="A family of
quokka" title="The quokka is an Australian
marsupial that is similar in size to the
domestic cat." />
```

* Height & Width
of Images

> You will also often see an < img>
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

> < img src="images/bird.gif" alt="Bird" width="100"
height="100" />
< p>There are around 10,000 living species of birds
that inhabit different ecosystems from the
Arctic to the Antarctic. Many species undertake
long distance annual migrations, and many more
perform shorter irregular journeys.</p>
< hr />
< p>< img src="images/bird.gif" alt="Bird" width="100"
height="100" />There are around 10,000 living
species of birds that inhabit different
ecosystems from the Arctic to the Antarctic. Many
species undertake long distance annual
migrations, and many more perform shorter
irregular journeys.< /p>
< hr />
< p>There are around 10,000 living species of birds
that inhabit different ecosystems from the
Arctic to the Antarctic.< img
src="images/bird.gif" alt="Bird" width="100"
height="100" />Many species undertake long
distance annual migrations, and many more perform
shorter irregular journeys.< /p> 

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

* Fi gure and
Fi gure Caption

> < figure>
Images often come with
captions. HTML5 has introduced
a new < figure> element to
contain images and their caption
so that the two are associated.
You can have more than one
image inside the < figure>
element as long as they all share
the same caption.
< figcaption>
The < figcaption> element has
been added to HTML5 in order
to allow web page authors to add
a caption to an image.
Before these elements were
created there was no way to
associate an < img> element with
its caption.
Older browsers that do not
understand HTML5 elements
simply ignore the new elements
and display the content of them.

```html
<figure>
<img src="images/otters.jpg" alt="Photograph of
two sea otters floating in water">
<br />
<figcaption>Sea otters hold hands when they
sleep so they don't drift away from each
other.</figcaption>
</figure>
```

* Summary
The < img> element is used to add images to a
web page.
* You must always specify a src attribute to indicate the
source of an image and an alt attribute to describe the
content of an image.
* You should save images at the size you will be using
them on the web page and in the appropriate format.
* Photographs are best saved as JPEGs; illustrations or
logos that use flat colors are better saved as GIFs.

---

**Chapter 11: “Color” (pp.246-263)**

* Background Color
background-color

> CSS treats each HTML element
as if it appears in a box, and the
background-color property
sets the color of the background
for that box.
You can specify your choice of
background color in the same
three ways you can specify
foreground colors: RGB values,
hex codes, and color names
(covered on the next page).
If you do not specify a
background color, then the
background is transparent.
By default, most browser
windows have a white
background, but browser users
can set a background color for
their windows, so if you want
to be sure that the background
is white you can use the
background-color property on
the < body> element.
We have also used the padding
property to separate the text
from the edges of the boxes.
This makes it easier to read and
you will learn more about this
property on page 313.

```css
body {
background-color: rgb(200,200,200);}
h1 {
background-color: DarkCyan;}
h2 {
background-color: #ee3e80;}
p {
background-color: white;}
```

* Opacity
opacity, rgba 

> CSS3 introduces the opacity
property which allows you to
specify the opacity of an element
and any of its child elements.
The value is a number between
0.0 and 1.0 (so a value of 0.5
is 50% opacity and 0.15 is 15%
opacity).
The CSS3 rgba property allows
you to specify a color, just like
you would with an RGB value,
but adds a fourth value to
indicate opacity. This value is
known as an alpha value and is
a number between 0.0 and 1.0
(so a value of 0.5 is 50% opacity
and 0.15 is 15% opacity). The
rgba value will only affect the
element on which it is applied
(not child elements).
Because some browsers will
not recognize RGBA colors, you
can offer a fallback so that they
display a solid color. If there are
two rules that apply to the same
element, the latter of the two
will take priority. To create the
fallback, you can specify a color
as a hex code, color name or
RGB value, followed by the rule
that specifies an RGBA value. If
the browser understands RGBA
colors it will use that rule. If it
doesn't, it will use the RGB value.
At the time of writing, the
opacity and rgba properties
are only supported by the most
recent browsers.

```css
p.one {
background-color: rgb(0,0,0);
opacity: 0.5;}
p.two {
background-color: rgb(0,0,0);
background-color: rgba(0,0,0,0.5);}
```

* CSS 3: HSL & HSLA
hsl, hsla

> The hsl color property has
been introduced in CSS3 as an
alternative way to specify colors.
The value of the property starts
with the letters hsl, followed
by individual values inside
parentheses for:
hue
This is expressed as an angle
(between 0 and 360 degrees).
saturation
This is expressed as a
percentage.
lightness
This is expressed as a
percentage with 0% being white,
50% being normal, and 100%
being black.
The hsla color property allows
you to specify color properties
using hue, saturation, and
lightness as above, and adds a
fourth value which represents
transparency (just like the rgba
property). The a stands for:
alpha
This is expressed as a
number between 0 and 1.0.
For example, 0.5 represents
50% transparency, and 0.75
represents 75% transparency.

```css
body {
background-color: #C8C8C8;
background-color: hsl(0,0%,78%);}
p {
background-color: #ffffff;
background-color: hsla(0,100%,100%,0.5);}
```

* summary 

* Color not only brings your s XX ite to life, but also helps
convey the mood and evokes reactions.
* There are three ways to specify colors in CSS:
RGB values, hex codes, and color names.
* Color pickers can help you find the color you want.
* It is important to ensure that there is enough contrast
between any text and the background color (otherwise
people will not be able to read your content).
* CSS3 has introduced an extra value for RGB colors to
indicate opacity. It is known as RGBA.
* CSS3 also allows you to specify colors as HSL values,
with an optional opacity value. It is known as HSLA.

----

**Chapter 12: “Text” (pp.264-299)**

* font-family

> The font-family property
allows you to specify the
typeface that should be used for
any text inside the element(s) to
which a CSS rule applies.
The value of this property is the
name of the typeface you want
to use.
The people who are visiting
your site need the typeface you
have specified installed on their
computer in order for it to be
displayed.
You can specify a list of fonts
separated by commas so that,
if the user does not have your
first choice of typeface installed,
the browser can try to use an
alternative font from the list.
It is also common to end with a
generic font name for that type
of font (which you saw on pages
269-270).
If a font name is made up of
more than one word, it should be
put in double quotes.
Designers suggest pages usually
look better if they use no more
than three typefaces on a page.
We will be using an extended
version of the HTML shown on
this page for all of the examples
in this chapter.

```html 
<!DOCTYPE html>
<html>
<head>
<title>Font Family</title>
<style type="text/css">
body {
font-family: Georgia, Times, serif;}
h1, h2 {
font-family: Arial, Verdana, sans-serif;}
.credits {
font-family: "Courier New", Courier,
monospace;}
</style>
</head>
<body>
<h1>Briards</h1>
<p class="credits">by Ivy Duckett</p>
<p class="intro">The <a class="breed"
href="http://en.wikipedia.org/wiki/
Briard">briard</a>, or berger de brie, is
a large breed of dog traditionally used as
a herder and guardian of sheep...</p>
</body>
</html>
```

* Bold
font-weight

> The font-weight property
allows you to create bold text.
There are two values that this
property commonly takes:
normal
This causes text to appear at a
normal weight.
bold
This causes text to appear bold.
In this example, you can see
that the element whose class
attribute has a value of credits
has been bolded.
You might wonder why there is
a normal weight. This is because
if, for example, you created a
rule for the < body> element
indicating that all text inside the
body should appear bold, you
might need an option that allows
the text in certain instances
to appear normal weight. So
it is essentially used as an "off
switch."

```css
.credits {
font-weight: bold;}
```

* font-style

> If you want to create italic text,
you can use the font-style
property. There are three values
this property can take:
normal
This causes text to appear in a
normal style (as opposed to italic
or oblique).
italic
This causes text to appear italic.
oblique
This causes text to appear
oblique.
In this example, you can see that
the credits have been italicized.
Italic fonts were traditionally
stylized versions of the font
based on calligraphy, whereas an
oblique version would take the
normal version and put it on an
angle.
It is not unusual for the browser
to fail to find an italic version of a
typeface, in which case it will use
an algorithm to place the normal
version of the type on a slant,
which means that a lot of italic
text online is actually oblique

```css
.credits {
font-style: italic;}
```

* text-decoration

> The text-decoration property
allows you to specify the
following values:
none
This removes any decoration
already applied to the text.
underline
This adds a line underneath the
text.
overline
This adds a line over the top of
the text.
line-through
This adds a line through words.
blink
This animates the text to make it
flash on and off (however this is
generally frowned upon, as it is
considered rather annoying).
In this example, the credits have
been underlined. Also, the name
of the breed (which is a link) is
not underlined, which it would
be by default because it is a link.
This property is commonly
used by designers to remove
the underlines that browsers
place under links. Pages 290-291
show how to add or remove an
underline when a user hovers
over a link.

``` css 
.credits {
text-decoration: underline;}
a {
text-decoration: none;}
```

* line-height

> Leading (pronounced ledding) is
a term typographers use for the
vertical space between lines of
text. In a typeface, the part of
a letter that drops beneath the
baseline is called a descender,
while the highest point of a letter
is called the ascender. Leading
is measured from the bottom of
the descender on one line to the
top of the ascender on the next.

``` css
p {
line-height: 1.4em;}
```

* letter-spacing, word-spacing

> Kerning is the term
typographers use for the space
between each letter. You can
control the space between each
letter with the letter-spacing
property.
It is particularly helpful to
increase the kerning when
your heading or sentence is
all in uppercase. If your text is
in sentence (or normal) case,
increasing or decreasing the
kerning can make it harder to
read.
You can also control the gap
between words using the
word-spacing property.
When you specify a value for
these properties, it should
be given in ems, and it will be
added on top of the default value
specified by the font.
The default gap between
words is set by the typeface
(often around 0.25em), and
it is unlikely that you would
need to change this property
regularly. If the typeface is bold
or you have increased the space
between letters, then a larger
gap between words can increase
readability

``` css
h1, h2 {
text-transform: uppercase;
letter-spacing: 0.2em;}
.credits {
font-weight: bold;
word-spacing: 1em;}
```

* Text - Align

> The text-align property allows
you to control the alignment of
text. The property can take one
of four values:
left
This indicates that the text
should be left-aligned.
right
This indicates that the text
should be right-aligned.
center
This allows you to center text.
justify
This indicates that every line in
a paragraph, except the last line,
should be set to take up the full
width of the containing box.
When you have several
paragraphs of text, it is
considered easiest to read if the
text is left-aligned.
Justified text looks at the words
on each individual line and
creates an equal gap between
those words. It can look odd
if you end up with large gaps
between some words and
smaller gaps between others.
This often happens when your
lines are not very wide or when
your text contains long words.

```css
h1 {
text-align: left;}
p {
text-align: justify;}
.credits {
text-align: right;}
```

* vertical-align
#six-

> The vertical-align property is
a common source of confusion.
It is not intended to allow you to
vertically align text in the middle
of block level elements such as
< p> and < div>, although it does
have this effect when used with
table cells (the < td> and < th>
elements).
It is more commonly used with
inline elements such as < img>,
< em>, or < strong> elements.
When used with these elements,
it performs a task very similar to
the HTML align attribute used
on the < img> element, which
you met on pages 103-106. The
values it can take are:

```css
#six-months {
vertical-align: text-top;}
#one-year {
vertical-align: baseline;}
#two-years {
vertical-align: text-bottom;}
```

-----

@AnasAhmad


