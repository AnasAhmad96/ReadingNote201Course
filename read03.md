# 201 Course 

![web developer](http://coderoo.com.au/blog/wp-content/uploads/2018/02/web.jpg)

----

| number      | subject |
| ----------- | ----------- |
| 1      |Chapter 3: “Lists” (pp.62-73)|
| 2   |Chapter 13: “Boxes” (pp.300-329)|
| 3   |Review from Reading 02 - Chapter 2: “Basic JavaScript Instructions” (pp.70-73)|
| 4   |Chapter 4: “Decisions and Loops” from switch statements on (pp.162-182)|

----

1- **Chapter 3: “Lists” (pp.62-73)”**

* Ordered Lists

> < ol >
The ordered list is created with
the < ol > element . <br>
>> < li >Each item in the list is placed
between an opening < li > tag
and a closing </li> tag. (The li
stands for list item.)
Browsers indent lists by default.
Sometimes you may see a type
attribute used with the < ol >
element to specify the type of
numbering (numbers, letters,
roman numerals and so on). It
is better to use the CSS list

```html
<ol>
<li>Chop potatoes into quarters</li>
<li>Simmer in salted water for 15-20
minutes until tender</li>
<li>Heat milk, butter and nutmeg</li>
<li>Drain potatoes and mash</li>
<li>Mix in the milk mixture</li>
</ol>
```

* Unordered Lists
> < ul > The unordered list is created
with the < ul > element.

```html
<ul>
<li>1kg King Edward potatoes</li>
<li>100ml milk</li>
<li>50g salted butter</li>
<li>Freshly grated nutmeg</li>
<li>Salt and pepper to taste</li>
</ul>
```
* Definition Lists

> < dl >
The definition list is created with
the < dl > element and usually
consists of a series of terms and
their definitions.
Inside the < dl > element you will
usually see pairs of < dt > and
< dd > elements.
< dt >
This is used to contain the term
being defined (the definition
term).
< dd >
This is used to contain the
definition.
Sometimes you might see a list
where there are two terms used
for the same definition or two
different definitions for the same
term.

```html
<dl>
<dt>Sashimi</dt>
<dd>Sliced raw fish that is served with
condiments such as shredded daikon radish or
ginger root, wasabi and soy sauce</dd>
<dt>Scale</dt>
<dd>A device used to accurately measure the
weight of ingredients</dd>
<dd>A technique by which the scales are removed
from the skin of a fish</dd>
<dt>Scamorze</dt>
<dt>Scamorzo</dt>
<dd>An Italian cheese usually made from whole
cow's milk (although it was traditionally made
from buffalo milk)</dd>
</dl>
```

* Nested Lists

> You can put a second list inside
an < li > element to create a sublist
or nested list.
Browsers display nested lists
indented further than the parent
list. In nested unordered lists,
the browser will usually change
the style of the bullet point too.

``` <ul>
<li>Mousses</li>
<li>Pastries
<ul>
<li>Croissant</li>
<li>Mille-feuille</li>
<li>Palmier</li>
<li>Profiterole</li>
</ul>
</li>
<li>Tarts</li>
</ul>
```

* summary
* There are three types of HTML lists: ordered,
unordered, and definition.
* Ordered lists use numbers.
* Unordered lists use bullets.
* Definition lists are used to define terminology.
* Lists can be nested inside one another.

----

**Chapter 13: “Boxes” (pp.300-329)**

* Border Style
border-style

```html
<p class="one">Wurlitzer Electric Piano</p>
<p class="two">Wurlitzer Electric Piano</p>
<p class="three">Wurlitzer Electric Piano</p>
<p class="four">Wurlitzer Electric Piano</p>
<p class="five">Wurlitzer Electric Piano</p>
<p class="six">Wurlitzer Electric Piano</p>
<p class="seven">Wurlitzer Electric Piano</p>
<p class="eight">Wurlitzer Electric Piano</p>
```

* BORDER WIDTH

```html
<p class="one">Hohner's "Clavinet" is essentially an
electric clavichord.</p>
<p class="two">Hohner's "Clavinet" is essentially an
electric clavichord.</p>
<p class="three">Hohner's "Clavinet" is essentially
an electric clavichord.</p>
```

* Border Color

```html
<p class="one">The ARP Odyssey was introduced in
1972.</p>
<p class="two">The ARP Odyssey was introduced in
1972.</p>
```
* Pading

```css
p {
width: 275px;
border: 2px solid #0088dd;}
p.example {
padding: 10px;}
```

* Margin

```css
p {
width: 200px;
border: 2px solid #0088dd;
padding: 10px;}
p.example {
margin: 20px;}
```
* summary
* CSS treats each HTML element as if it has its own box.
* You can use CSS to control the dimensions of a box.
* You can also control the borders, margin and padding
for each box with CSS.
* It is possible to hide elements using the display and
visibility properties.
* Block-level boxes can be made into inline boxes, and
inline boxes made into block-level boxes.
* Legibility can be improved by controlling the width of
boxes containing text and the leading.
* CSS3 has introduced the ability to create image
borders and rounded borders.

----

**Review from Reading 02 - Chapter 2: “Basic JavaScript Instructions” (pp.70-73)**

* USING A VARIABLE TO
STORE A BOOLEAN

```js
var i nStock;
var shipping;
inStock = true;
shipping= fa l se;
JAVASCRIPT
var elStock = document.getElementByld('stock');
elStock.className = inStock;
var el Ship = document .getElementByid('shipping');
elShip.className = shipping ;
```

* SHORTHAND FOR
CREATING VARIABLES

```js
var price = 5;
var quantity = 14;
var total = price * quantity;
```

* CHANGING THE VALUE
OF A VARIABLE

```js
var inStock;
var shipping;
inStock = true;
shipping = false;
JAVASCRIPT
/* Some other processing might go here and , as
a resul t , the script might need to change t hese
values */
inStock = false;
shipping = true;
var elStock = document.getElementByld('stock');
elStock .className = inStock;
var elShip = document .getElementByld('shipping');
elShip .className = shipping;
```
----

**Chapter 4: “Decisions and Loops” from switch statements on (pp.162-182)**

* Logical Operator

> & and
>> || or 
>>> ! not

```js
var scorel = 8; II Round 1 score
var score2 = 8; II Round 2 score
var passl 6; II Round 1 pass mark
var pass2 = 6; II Round 2 pass mark
II Check whether user passed both rounds , store result in variable
var passBoth = (scorel >= passl) && (score2 >= pass2);
II Create message
var msg = 'Both rounds passed: ' + passBoth;
II Write the message i nto the page
var el = document.getElementBy!d( ' answer') ;
el.textContent = msg;
```

* USING IF STATEMENTS

```js
var score 75; II Score
var msg; II Message
if (score>= 50) { II If score is 50 or higher
msg = 'Congratulations!';
msg += ' Proceed to the next round . ' ;
var el = document.getElementByld('answer ' ) ;
el .textContent = msg;
```

* USING IF ... ELSE
STATEMENTS

```js
var pass = 50;
var score = 75;
var msg;
II Pass mark
II Current score
II Message
II Select message to write based on score
if (score >= pass) {
msg = 'Congratulations, you passed!';
} else {
msg = 'Have another go!';
var el = document .getElementByld('answer');
el .textContent = msg;
```

* USING SWITCH
STATEMENTS

```js
var msg;
var level = 2;
II Message
11 Level
c04/js/switch-statement .js
/I Determine message based on level
switch (level) {
case 1:
msg = 'Good luck on the first test ' ;
break;
case 2:
msg = 'Second of three - keep going!';
break;
case 3:
msg = ' Final round, almost there!';
break;
default :
msg = 'Good l uck!';
break;
var el = document.getEl ementByld('answer ' );
el .textContent = msg;
```

* USING FOR LOOPS

```js
var scores= [24. 32, 17]; //Array of scores
var arraylength scores .l ength;// Items in array
var roundNumber = O; //Current round
var msg ''; //Message
var i ; // Counter
//Loop through the items in the array
for (i = O; i < arraylength; i++) {
//Arrays are zero based (so 0 is round 1)
//Add 1 to the current round
roundNumber = (i + l);
// Write the current round to message
msg += 'Round ' + roundNumber + ' : ';
//Get the score from the scores array
msg += scores[i] + '<br / >' ;
document .getElementByid( ' answer') .i nnerHTML msg;
```

----

@AnasAhmad