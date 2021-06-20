# 201 Course 
![web developer](http://coderoo.com.au/blog/wp-content/uploads/2018/02/web.jpg)
----

| number      | subject |
| ----------- | ----------- |
| 1      | Chapter 2: “Text” (pp.40-61)|
| 2   | Chapter 10: Ch.10 “Introducing CSS” (pp.226-245)|
| 3   |Chapter 2: “Basic JavaScript Instructions” (pp.53-84)|
| 4   |Chapter 4: “Decisions and Loops” (pp.145-162)|

----
1- **Chapter 2: “Text”**
### Headings
```html
<h1>This is a Main Heading</h1>
<h2>This is a Level 2 Heading</h2>
<h3>This is a Level 3 Heading</h3>
<h4>This is a Level 4 Heading</h4>
<h5>This is a Level 5 Heading</h5>
<h6>This is a Level 6 Heading</h6>
```

> HTML has six "levels" of
headings:
< h1> is used for main headings
< h2> is used for subheadings
If there are further sections
under the subheadings then the
< h3> element is used, and so
on...
Browsers display the contents of
headings at different sizes. The
contents of an < h1> element is
the largest, and the contents of
an < h6> element is the smallest.
The exact size at which each
browser shows the headings
can vary slightly. Users can also
adjust the size of text in their
browser. You will see how to
control the size of text, its color,
and the fonts used when we
come to look at CSS.
-----
### Paragraphs
```html
<p>Text is easier to understand when it is split up
into units of text. For example, a book may have
chapters. Chapters can have subheadings. Under
each heading there will be one or more
paragraphs.</p>
```
> To create a paragraph, surround
the words that make up the
paragraph with an opening <p>
tag and closing </p> tag.
By default, a browser will show
each paragraph on a new line
with some space between it and
any subsequent paragraphs.
-----
### Bold & Italic 
```html 
<p>This is how we make a word appear <b>bold.</b>
</p>
<p>This is how we make a word appear <i>italic</i>.
</p>
```
> < b>
By enclosing words in the tags
<b> and </b> we can make
characters appear bold.
The <b> element also represents
a section of text that would be
presented in a visually different
way (for example key words in a
paragraph) although the use of
the <b> element does not imply
any additional meaning.
>> < i>
By enclosing words in the tags
<i> and </i> we can make
characters appear italic.
The <i> element also represents
a section of text that would be
said in a different way from
surrounding content — such as
technical terms, names of ships,
foreign words, thoughts, or other
terms that would usually be
italicized.
-----
### Superscript & Subscript
``` html 
<p>On the 4<sup>th</sup> of September you will learn
about E=MC<sup>2</sup>.</p>
<p>The amount of CO<sub>2</sub> in the atmosphere
grew by 2ppm in 2009<sub>1</sub>.</p>
```
> < sup>
The <sup> element is used
to contain characters that
should be superscript such
as the suffixes of dates or
mathematical concepts like
raising a number to a power such
as 22.
>> < sub>
The <sub> element is used to
contain characters that should
be subscript. It is commonly
used with foot notes or chemical
formulas such as H20.
-----
### White Space
``` html 
<p>The moon is drifting away from Earth.</p>
<p>The moon is drifting away from Earth.</p>
<p>The moon is drifting away from
Earth.</p>
```
> In order to make code easier to
read, web page authors often
add extra spaces or start some
elements on new lines.
When the browser comes across
two or more spaces next to each
other, it only displays one space.
Similarly if it comes across a line
break, it treats that as a single
space too. This is known as
white space collapsing.
You will often see that web page
authors take advantage of white
space collapsing to indent their
code in order to make it easier
to follow.
-----
#### Line Breaks & Horizontal Rules
``` html
<p>The Earth<br />gets one hundred tons heavier
every day<br />due to falling space dust.</p>

<p>Venus is the only planet that rotates
clockwise.</p>
<hr />
<p>Jupiter is bigger than all the other planets
```
> < br />
As you have already seen, the
browser will automatically show
each new paragraph or heading
on a new line. But if you wanted
to add a line break inside the
middle of a paragraph you can
use the line break tag <br />.
>> To create a break between
themes — such as a change of
topic in a book or a new scene
in a play — you can add a
horizontal rule between sections
using the <hr /> tag.
There are a few elements that
do not have any words between
an opening and closing tag. They
are known as empty elements
and they are written differently.
----
### Strong & Emphasis
``` html
<p><strong>Beware:</strong> Pickpockets operate in
this area.</p>

<p>I <em>think</em> Ivy was the first.</p>
```
> < strong>
The use of the <strong>
element indicates that its
content has strong importance.
For example, the words
contained in this element might
be said with strong emphasis.
By default, browsers will show
the contents of a <strong>
element in bold.
>> < em>
The <em> element indicates
emphasis that subtly changes
the meaning of a sentence.
By default browsers will show
the contents of an <em> element
in italic.
------
2- **Chapter 10: Ch.10 “Introducing CSS” (pp.226-245)**
1. inline
1. external
1. internal
> CSS allows you to create rules that control the
way that each individual box (and the contents
of that box) is presented.

>> CSS works by associating rules with HTML elements. These rules govern
how the content of specified elements should be displayed. A CSS rule
contains two parts: a selector and a declaration.
>>> CSS declarations sit inside curly brackets and each is made up of two
parts: a property and a value, separated by a colon. You can specify
several properties in one declaration, each separated by a semi-colon.
``` css
<!DOCTYPE html>
<html>
<head>
<title>Introducing CSS</title>
<link href="css/example.css" type="text/css"
rel="stylesheet" />
</head>
<body>
<h1>From Garden to Plate</h1>
<p>A <i>potager</i> is a French term for an
ornamental vegetable or kitchen garden ... </p>
<h2>What to Plant</h2>
<p>Plants are chosen as much for their functionality
as for their color and form ... </p>
</body>
</html>
body {
font-family: Arial, Verdana, sans-serif;}
h1, h2 {
color: #ee3e80;}
p {
color: #665544;}
```
CSS treats each HTML 
* lement as if it appears inside
its own box and uses rules to indicate how that
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
-----
3- Chapter 2: “Basic JavaScript Instructions” (pp.53-84)

How do i write a script for web page ?
* It is best to keep JavaScript code in its own JavaScriptfile. 
* JavaScript files are text files (like HTML pages and
CSS style sheets), but they have the . js extension.
* The HTML < script> element is used in HTML pages
to tell the browser to load the JavaScript file (rather like
* the < link> element can be used to load a CSS file).
If you view the source code of the page in the browser,
the JavaScript will not have changed the HTML,
because the script works with the model of the web
page that the browser has created.
---
### COMMENTS
``` js
I* Th i s script displays a greeting to the user based upon the current time.
It is an example from JavaScript & jQuery book *I
var today= new Date();
var hour Now = today.getHours();
var greeting;
// Create a ne1~ dat e object
II Fi nd the current hour
JI Display the appropriate greeti ng based on the current time
if (hourNow > 18) {
greet ing = 'Good evening ' ;
else if (hourNow > 12) {
greeting = 'Good afternoon';
else if (hourNow > 0) {
greeting= ' Good morning';
else {
gr eeting = 'Welcome';
}
document.write(greeting) ;
```
----
``` js
II PART TWO: CALCULATE ANO WRITE OUT THE EX PIRY DETAILS FOR THE OFFER
var expiryMsg; II Message displ ayed t o users
var today ; II Today's date
var el Ends ; II The element that shows the mes sage about the offer endi ng
function of fer Expires (today) {
II Decl are variables within the functi on for l ocal scope
var weekFromToday, day, date, month, year, dayNames, monthNames;
II Add 7 days time (added in mi l li seconds)
weekFromToday =new Dat e(today .getTi me () + 7 * 24 * 60 * 60 * 1000) ;
II Create arrays to hold t he names of days I months
dayNames = [ ' Sunday' , ' Monday' , 'Tuesday ' , 'Wednesday ', 'Thursday' ,
0 ' Friday', 'Saturday ' ] ;
mont hNames =[' January', ' Februa ry', 'March', ' Apri l ', 'May ' , ' June ' ,
0 ' Jul y' , 'August ' , 'September' , 'October' , ' November' , 'December ' ] ;
II Collect the parts of the date to show on t he page
day = dayNames [weekFromToday . getOay ()];
date= weekFromToday .getOate();
month= mont hNames[weekFromToday.getMonth()] ;
year= weekFromToday .getFullYear() ;
II Create the message
expi ryMsg = 'Offer expires next ' ;
expi ryMsg += day + ' <br I>( ' +date+ ' ' +month+ ' ' +year + ')';
retu rn expiryMsg;
today= new Date() ;
elEnds = document .getEl ementByid( 'off erEnds');
elEnds .i nnerHTML = offe rExpires(today) ;
II Put today's date in vari able
II Get t he offe r Ends el ement
II Add t he expi ry message
II Finish the immediately i nvoked functi on exp ression
} () ) ;
```
-----
* Functions allow you to group a set of related
statements together that represent a single task.
* Functions can take parameters (informatiorJ required
to do their job) and may return a value.
* An object is a series of variables and functions that
represent something from the world around you.
* In an object, variables are known as properties of the
object; functions are known as methods of the object.
* Web browsers implement objects that represent both
the browser window and the document loaded into the
browser window.
* JavaScript also has several built-in objects such as
String, Number, Math, and Date. Their properties and
methods offer functionality that help you write scripts.
* Arrays and objects can be used to create complex data
sets (and both can contain the other).
----
@AnasAhmad