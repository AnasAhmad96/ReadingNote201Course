# 201 Course

![web developer](http://coderoo.com.au/blog/wp-content/uploads/2018/02/web.jpg)

----

| number      | subject |
| ----------- | ----------- |
| 1   |Chapter 7: “Forms” (p.144-175)|
| 2   |Chapter 14: “Lists, Tables & Forms” (pp.330-357)|
| 3   |Chapter 6: “Events” (pp.243-292)|

----

# Forms

**Form Controls**

* ADDING TEXT:
* Password input
* Text area (multi-line)
* Making Choices
* Checkboxes
* Drop-down boxes
* Submitting Forms
* Uploading Files
* Image buttons

*Form Structure*

> < form>
Form controls live inside a
< form> element. This element
should always carry the action
attribute and will usually have a
method and id attribute too.
action
Every < form> element requires
an action attribute. Its value
is the URL for the page on the
server that will receive the
information in the form when it
is submitted.
method
Forms can be sent using one of
two methods: get or post.
With the get method, the values
from the form are added to
the end of the URL specified in
the action attribute. The get
method is ideal for:
●● short forms (such as search
boxes)
●● when you are just retrieving
data from the web server
(not sending information that
should be added to or deleted
from a database)

```html
<form action="http://www.example.com/subscribe.php"
method="get">
<p>This is where the form controls will appear.
</p>
</form>
```

* Text Input

> < input>
The < input> element is used
to create several different form
controls. The value of the type
attribute determines what kind
of input they will be creating.
type="text"
When the type attribute has a
value of text, it creates a singleline
text input.
name
When users enter information
into a form, the server needs to
know which form control each
piece of data was entered into.
(For example, in a login form, the
server needs to know what has
been entered as the username
and what has been given as the
password.) Therefore, each form
control requires a name attribute.
The value of this attribute
identifies the form control and is
sent along with the information
they enter to the server.
maxlength
You can use the maxlength
attribute to limit the number
of characters a user may enter
into the text field. Its value is the
number of characters they may
enter. For example, if you were
asking for a year, the maxlength
attribute could have a value of 4.

```html
<form action="http://www.example.com/login.php">
<p>Username:
<input type="text" name="username" size="15"
maxlength="30" />
</p>
</form>
```

*Password Input*

> < input>
type="password"
When the type attribute has
a value of password it creates
a text box that acts just like a
single-line text input, except
the characters are blocked out.
They are hidden in this way so
that if someone is looking over
the user's shoulder, they cannot
see sensitive data such as
passwords.
name
The name attribute indicates
the name of the password input,
which is sent to the server with
the password the user enters.
size, maxlength
It can also carry the size and
maxlength attributes like the
the single-line text input.

```html
<form action="http://www.example.com/login.php">
<p>Username:
<input type="text" name="username" size="15"
maxlength="30" />
</p>
<p>Password:
<input type="password" name="password" size="15"
maxlength="30" />
</p>
</form>
```

*Text Area*

> < textarea>
The < textarea> element
is used to create a mutli-line
text input. Unlike other input
elements this is not an empty
element. It should therefore have
an opening and a closing tag.
Any text that appears between
the opening < textarea> and
closing < /textarea> tags will
appear in the text box when the
page loads.
If the user does not delete any
text between these tags, this
message will get sent to the
server along with whatever the
user has typed. (Some sites
use JavaScript to clear this
information when the user clicks
in the text area.)

```html
<form action="http://www.example.com/comments.php">
<p>What did you think of this gig?</p>
<textarea name="comments" cols="20" rows="4">Enter
your comments...</textarea>
</form>
```

*Radio Button*

> < input>
type="radio"
Radio buttons allow users to pick
just one of a number of options.
name
The name attribute is sent to
the server with the value of the
option the user selects. When
a question provides users with
options for answers in the form
of radio buttons, the value of
the name attribute should be the
same for all of the radio buttons
used to answer that question.
value
The value attribute indicates
the value that is sent to the
server for the selected option.
The value of each of the buttons
in a group should be different
(so that the server knows which
option the user has selected).
checked
The checked attribute can be
used to indicate which value (if
any) should be selected when
the page loads. The value of this
attribute is checked. Only one
radio button in a group should
use this attribute.

```html
<form action="http://www.example.com/profile.php">
<p>Please select your favorite genre:
<br />
<input type="radio" name="genre" value="rock"
checked="checked" /> Rock
<input type="radio" name="genre" value="pop" />
Pop
<input type="radio" name="genre" value="jazz" />
Jazz
</p>
</form>
```

*CHECKBOX*

>< input>
type="checkbox"
Checkboxes allow users to select
(and unselect) one or more
options in answer to a question.
name
The name attribute is sent to
the server with the value of the
option(s) the user selects. When
a question provides users with
options for answers in the form
of checkboxes, the value of the
name attribute should be the
same for all of the buttons that
answer that question.
value
The value attribute indicates
the value sent to the server if this
checkbox is checked.
checked
The checked attribute indicates
that this box should be checked
when the page loads. If used, its
value should be checked.

```html
<form action="http://www.example.com/profile.php">
<p>Please select your favorite music service(s):
<br />
<input type="checkbox" name="service"
value="itunes" checked="checked" /> iTunes
<input type="checkbox" name="service"
value="lastfm" /> Last.fm
<input type="checkbox" name="service"
value="spotify" /> Spotify
</p>
</form>
```

*Drop Down Li st Box*

> < select>
A drop down list box (also
known as a select box) allows
users to select one option from a
drop down list.
The < select> element is used
to create a drop down list box. It
contains two or more < option>
elements.
name
The name attribute indicates the
name of the form control being
sent to the server, along with the
value the user selected.
< option>
The < option> element is used
to specify the options that the
user can select from. The words
between the opening < option>
and closing < /option> tags will
be shown to the user in the drop
down box.
value
The < option> element uses the
value attribute to indicate the
value that is sent to the server
along with the name of the
control if this option is selected.

```html
<form action="http://www.example.com/profile.php">
<p>What device do you listen to music on?</p>
<select name="devices">
<option value="ipod">iPod</option>
<option value="radio">Radio</option>
<option value="computer">Computer</option>
</select>
</form>
```

*Multiple Se lec t Box*

> < select>
size
You can turn a drop down select
box into a box that shows more
than one option by adding the
size attribute. Its value should
be the number of options you
want to show at once. In the
example you can see that three
of the four options are shown.
Unfortunately, the way that
browsers have implemented this
attribute is not perfect, and it
should be tested throroughly if
used (in particular in Firefox and
Safari on a Mac).
multiple
You can allow users to select
multiple options from this list by
adding the multiple attribute
with a value of multiple.
It is a good idea to tell users if
they can select more than one
option at a time. It is also helpful
to indicate that on a PC they
should hold down the control key
while selecting multiple options
and on a Mac they should use
the command key while selecting
options.

```html
<form action="http://www.example.com/profile.php">
<p>Do you play any of the following instruments?
(You can select more than one option by holding
down control on a PC or command key on a Mac
while selecting different options.)</p>
<select name="instruments" size="3"
multiple="multiple">
<option value="guitar" selected="selected">
Guitar</option>
<option value="drums">Drums</option>
<option value="keyboard"
selected="selected">Keyboard</option>
<option value="bass">Bass</option>
</select>
</form>
```

**Summary**

* Whenever you want to c XX ollect information from
visitors you will need a form, which lives inside a
< form> element.
* Information from a form is sent in name/value pairs.
* Each form control is given a name, and the text the
* user types in or the values of the options they select
are sent to the server.
* HTML5 introduces new form elements which make it
easier for visitors to fill in forms.

-----

# Lists, Tables & Forms

* Table Proparties

```html
<h1>First Edition Auctions</h1>
<table>
<tr>
<th>Author</th>
<th>Title</th>
<th class="money">Reserve Price</th>
<th class="money">Current Bid</th>
</tr>
<tr>
<td>E.E. Cummings</td>
<td>Tulips & Chimneys</td>
<td class="money">$2,000.00</td>
<td class="money">$2,642.50</td>
</tr>
<tr class="even">
<td>Charles d'Orleans</td>
<td>Poemes</td>
<td class="money"></td>
<td class="money">$5,866.00</td>
</tr>
<tr>
<td>T.S. Eliot</td>
<td>Poems 1909 - 1925</td>
<td class="money">$1,250.00</td>
<td class="money">$8,499.35</td>
</tr>
<tr class="even">
<td>Sylvia Plath</td>
<td>The Colossus</td>
<td class="money"></td>
<td class="money">$1031.72</td>
</tr>
</table>
```

* Border on Empty Cells

> If you have empty cells in
your table, then you can use
the empty-cells property to
specify whether or not their
borders should be shown.
Since browsers treat empty cells
in different ways, if you want to
explicitly show or hide borders
on any empty cells then you
should use this property.
It can take one of three values:
show
This shows the borders of any
empty cells.
hide
This hides the borders of any
empty cells.
inherit
If you have one table nested
inside another, the inherit
value instructs the table cells to
obey the rules of the containing
table.
In the first table on the left, you
can see that the border of the
empty cell is showing. In the
second table, it is hidden.

```html
<table class="one">
<tr>
<td>1</td>
<td>2</td>
</tr>
<tr>
<td>3</td>
<td></td>
</tr>
</table>
```

* Styling Text

```css
input {
font-size: 120%;
color: #5a5854;
background-color: #f2f2f2;
border: 1px solid #bdbdbd;
border-radius: 5px;
padding: 5px 5px 5px 30px;
background-repeat: no-repeat;
background-position: 8px 9px;
display: block;
margin-bottom: 10px;}
input:focus {
background-color: #ffffff;
border: 1px solid #b1e1e4;}
input#email {
background-image: url("images/email.png");}
input#twitter {
background-image: url("images/twitter.png");}
input#web {
background-image: url("images/web.png");}
```

* Styling Submit Buttons

> Here are some properties that
can be used to style submit
buttons. This example builds
on the one in the previous page,
and the submit button inherits
the styles set for the <input>
element on the last page.
color is used to change the
color of the text on the button.
text-shadow can give a 3D
look to the text in browsers that
support this property.
border-bottom has been used
to make the bottom border of
the button slightly thicker, which
gives it a more 3D feel.
background-color can make
the submit button stand out
from other items around it.
(Creating a consistent style
for all buttons helps users
understand how they should
interact with the site.) A gradient
background has been added for
browsers that support gradients.
Gradients are covered on
page 419.
The :hover pseudo-class
has been used to change the
appearance of the button when
the user hovers over it. In this
case, the background changes,
the text gets darker, and the
thicker border is applied to the
top of the button.

```css
input#submit {
color: #444444;
text-shadow: 0px 1px 1px #ffffff;
border-bottom: 2px solid #b2b2b2;
background-color: #b9e4e3;
background: -webkit-gradient(linear, left top,
left bottom, from(#beeae9), to(#a8cfce));
background:
-moz-linear-gradient(top, #beeae9, #a8cfce);
background:
-o-linear-gradient(top, #beeae9, #a8cfce);
background:
-ms-linear-gradient(top, #beeae9, #a8cfce);}
input#submit:hover {
color: #333333;
border: 1px solid #a4a4a4;
border-top: 2px solid #b2b2b2;
background-color: #a0dbc4;
background: -webkit-gradient(linear, left top,
left bottom, from(#a8cfce), to(#beeae9));
background:
-moz-linear-gradient(top, #a8cfce, #beeae9);
background:
-o-linear-gradient(top, #a8cfce, #beeae9);
background:
-ms-linear-gradient(top, #a8cfce, #beeae9);}
```

* summary

* In addition to the CSS p XX roperties covered in other
chapters which work with the contents of all elements,
there are several others that are specifically used to
control the appearance of lists, tables, and forms.
* List markers can be given different appearances
using the list-style-type and list-style image
properties.
* Table cells can have different borders and spacing in
different browsers, but there are properties you can
use to control them and make them more consistent.
* Forms are easier to use if the form controls are
vertically aligned using CSS.
* Forms benefit from styles that make them feel more
interactive.

-------

# Events

* Summary

* The browser represents the page using a DOM tree.
* DOM trees have four types of nodes: document nodes,
element nodes, attribute nodes, and text nodes.
* You can select element nodes by their id or cl ass
attributes, by tag name, or using CSS selector syntax.
* Whenever a DOM query can return more than one
node, it will always return a Nadel i st.
* From an element node, you can access and update its
content using properties such as textContent and
i nnerHTML or using DOM manipulation techniques.
* An element node can contain multiple text nodes and
child elements that are siblings of each other.
* In older browsers, implementation of the DOM is
inconsistent (and is a popular reason for using jQuery).
* Browsers offer tools for viewing the DOM tree .

-------

@AnasAhmad
