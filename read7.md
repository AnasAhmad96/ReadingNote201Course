# 201 Course 

![web developer](http://coderoo.com.au/blog/wp-content/uploads/2018/02/web.jpg)

----

| number      | subject |
| ----------- | ----------- |
| 1   |Understanding The Problem Domain Is The Hardest Part Of Programming|
| 2   |Chapter 3: “Object Literals” (pp.100-105)|
| 3   |Chapter 5: “Document Object Model” (pp.183-242)|

----

**Table**

* Basic Table St ructure

>< table>
The < table> element is used
to create a table. The contents
of the table are written out row
by row.
< tr>
You indicate the start of each
row using the opening < tr> tag.
(The tr stands for table row.)
It is followed by one or more
< td> elements (one for each cell
in that row).
At the end of the row you use a
closing < /tr> tag.
< td>
Each cell of a table is
represented using a < td>
element. (The td stands for
table data.)
At the end of each cell you use a
closing < /td> tag.

```html
<table>
<tr>
<td>15</td>
<td>15</td>
<td>30</td>
</tr>
<tr>
<td>45</td>
<td>60</td>
<td>45</td>
</tr>
<tr>
<td>60</td>
<td>90</td>
<td>90</td>
</tr>
</table>
```

* Table Headings 

> < th>
The < th> element is used just
like the < td> element but its
purpose is to represent the
heading for either a column or
a row. (The th stands for table
heading.)
Even if a cell has no content,
you should still use a < td> or
< th> element to represent
the presence of an empty cell
otherwise the table will not
render correctly. (The first cell
in the first row of this example
shows an empty cell.)
Using < th> elements for
headings helps people who
use screen readers, improves
the ability for search engines
to index your pages, and also
enables you to control the
appearance of tables better
when you start to use CSS.
You can use the scope attribute
on the < th> element to indicate
whether it is a heading for a
column or a row. It can take the
values: row to indicate a heading
for a row or col to indicate a
heading for a column.
Browsers usually display the
content of a < th> element in
bold and in the middle of the cell.

```html
<table>
<tr>
<th></th>
<th scope="col">Saturday</th>
<th scope="col">Sunday</th>
</tr>
<tr>
<th scope="row">Tickets sold:</th>
<td>120</td>
<td>135</td>
</tr>
<tr>
<th scope="row">Total sales:</th>
<td>$600</td>
<td>$675</td>
</tr>
</table>
```

* Spanning ColumnS

>Sometimes you may need the
entries in a table to stretch
across more than one column.
The colspan attribute can be
used on a < th> or < td> element
and indicates how many columns
that cell should run across.
In the example on the right
you can see a timetable with
five columns; the first column
contains the heading for that
row (the day), the remaining four
represent one hour time slots.
If you look at the table cell that
contains the words 'Geography'
you will see that the value of the
colspan attribute is 2, which
indicates that the cell should run
across two columns. In the third
row, 'Gym' runs across three
columns.
You can see that the second
and third rows have fewer
< td> elements than there are
columns. This is because, when
a cell extends across more than
one column, the < td> or < th>
cells that would have been in the
place of the wider cells are not
included in the code.

```html
<table>
<tr>
<th></th>
<th>9am</th>
<th>10am</th>
<th>11am</th>
<th>12am</th>
</tr>
<tr>
<th>Monday</th>
<td colspan="2">Geography</td>
<td>Math</td>
<td>Art</td>
</tr>
<tr>
<th>Tuesday</th>
<td colspan="3">Gym</td>
<td>Home Ec</td>
</tr>
</table>
```

* Spanning Rows

> You may also need entries in
a table to stretch down across
more than one row.
The rowspan attribute can be
used on a < th> or < td> element
to indicate how many rows a cell
should span down the table.
In the example on the left you
can see that ABC is showing a
movie from 6pm - 8pm, whereas
the BBC and CNN channels are
both showing two programs
during this time period (each of
which lasts one hour).
If you look at the last < tr>
element, it only contains three
elements even though there are
four columns in the result below.
This is because the movie in the
< tr> element above it uses the
rowspan attribute to stretch
down and take over the cell
below.

```html
<table>
<tr>
<th></th>
<th>ABC</th>
<th>BBC</th>
<th>CNN</th>
</tr>
<tr>
<th>6pm - 7pm</th>
<td rowspan="2">Movie</td>
<td>Comedy</td>
<td>News</td>
</tr>
<tr>
<th>7pm - 8pm</th>
<td>Sport</td>
<td>Current Affairs</td>
</tr>
</table>
```

* Long Tables

> There are three elements that
help distinguish between the
main content of the table and
the first and last rows (which can
contain different content).
These elements help people
who use screen readers and also
allow you to style these sections
in a different manner than the
rest of the table (as you will see
when you learn about CSS).
< thead>
The headings of the table should
sit inside the < thead> element.
< tbody>
The body should sit inside the
< tbody> element.
< tfoot>
The footer belongs inside the
< tfoot> element.
By default, browsers rarely treat
the content of these elements
any differently than other
elements however designers
often use CSS styles to change
their appearance.

```html
<table>
<thead>
<tr>
<th>Date</th>
<th>Income</th>
<th>Expenditure</th>
</tr>
</thead>
<tbody>
<tr>
<th>1st January</th>
<td>250</td>
<td>36</td>
</tr>
<tr>
<th>2nd January</th>
<td>285</td>
<td>48</td>
</tr>
<!-- additional rows as above -->
<tr>
<th>31st January</th>
<td>129</td>
<td>64</td>
</tr>
</tbody>
<tfoot>
<tr>
<td></td>
<td>7824</td>
<td>1241</td>
</tr>
</tfoot>
</table>
```

* Width & Spacing

> There are some outdated
attributes which you should not
use on new websites. You may,
however, come across some
of them when looking at older
code, so I will mention them
here. All of these attributes have
been replaced by the use of CSS.
The width attribute was used
on the opening < table> tag to
indicate how wide that table
should be and on some opening
< th> and < td> tags to specify
the width of individual cells.
The value of this attribute is
the width of the table or cell in
pixels.
The columns in a table need to
form a straight line, so you often
only see the width attribute on
the first row (and all subsequent
rows would use that setting).
The opening < table> tag could
also use the cellpadding
attribute to add space inside
each cell of the table, and the
cellspacing attribute to create
space between each cell of
the table. The values for these
attributes were given in pixels.

```html
<table width="400" cellpadding="10" cellspacing="5">
<tr>
<th width="150"></th>
<th>Withdrawn</th>
<th>Credit</th>
<th width="150">Balance</th>
</tr>
<tr>
<th>January</th>
<td>250.00</td>
<td>660.50</td>
<td>410.50</td>
</tr>
<tr>
<th>February</th>
<td>135.55</td>
<td>895.20</td>
<td>1170.15</td>
</tr>
</table>
```

* Border & Background

> The border attribute was used
on both the < table> and < td>
elements to indicate the width of
the border in pixels.
The bgcolor attribute was used
to indicate background colors
of either the entire table or
individual table cells. The value
is usually a hex code (which we
discuss on pages 249-252).
This example uses the HTML
border and bgcolor attributes.
No CSS attributes were utilized
in this example.
When building a new website
you should use CSS to control
the appearance of the table
rather than these attributes.
They are only covered here
because you may come across
them if you look at the code of
older websites

```html 
<table border="2" bgcolor="#efefef">
<tr>
<th width="150"></th>
<th>Withdrawn</th>
<th>Credit</th>
<th width="150" bgcolor="#cccccc">Balance</th>
</tr>
<tr>
<th>January</th>
<td>250.00</td>
<td>660.50</td>
<td bgcolor="#cccccc">410.50</td>
</tr>
<tr>
<th>February</th>
<td>135.55</td>
<td>895.20</td>
<td bgcolor="#cccccc">1170.15</td>
</tr>
</table>
````

* Summary 

* The < table> element is used to add tables to a web
page.
* A table is drawn out row by row. Each row is created
with the < tr> element.
* Inside each row there are a number of cells
represented by the < td> element (or < th> if it is a
header).
* You can make cells of a table span more than one row
or column using the rowspan and colspan attributes.
* For long tables you can split the table into a < thead>,
< tbody>, and < tfoot>.

-----

* CREATING· OBJECTS USING
LITERAL NOTATION 

```js
var hotel = {
name: 'Quay',
rooms : 40,
booked: 25,
checkAvailability: function() {
return this.rooms - this.booked;
}
} ;
JAVASCRIPT
var elName = document .getElementByld('hotelName');
elName.textContent =hotel .name;
var elRooms = document.getElementByid{'rooms');
elRooms .textContent = hotel .checkAvailability();
```

* CREATING OBJECTS USING
CONSTRUCTOR SYNTAX

```js
var hotel = new Object();
hotel.name= 'Park';
hotel.rooms = 120;
hotel .booked = 77;
hotel .checkAvailability = function()
return this . rooms - this.booked;
} ;
JAVASCRIPT
var elName = document.getElementByid('hotelName');
elName.textContent = hotel . name;
var elRooms = document .getElementByid('rooms');
elRooms .textContent = hotel .checkAvailability(};
```

* CREATE & ACCESS OBJECTS
CONSTRUCTOR NOTATION 

```js
function Hotel (name, rooms, booked) {
this .name = name;
this.rooms = rooms;
this.booked = booked;
this.checkAvailability = function()
return this.rooms - this.booked;
} ;
var quayHotel
var parkHotel
new Hotel('Quay', 40, 25);
new Hotel( ' Park', 120, 77);
var details!= quayHotel .name + ' rooms : ';
detailsl += quayHotel.checkAvailability();
var elHotell = docurnent.getElementByid('hotell');
elHotell.textContent =details!;
var details2 = parkHotel .name+ ' rooms: ';
detai l s2 += parkHotel.checkAvailability();
var e1Hotel2 = document.getEl ementByid('hotel2');
elHotel2.textContent = details2;
```

* ADDING AND REMOVING
PROPERTIES 

```js 
var hotel = {
name : 'Park' ,
rooms : 120,
booked : 77.
} ;
hotel .gym = t rue;
hotel .pool = fal se;
delete hotel .booked;
var elName = document .getEl ementByld('hotelName ' );
elName.textContent = hotel . name;
var el Pool = document .getElementByid ('pool ') ;
elPool.cl assName = ' Pool: ' + hotel. pool ;
var elGym = document .getEl ementByld('gym ' };
elGym.className = 'Gym: ' + hotel .gym;
```

* FUNCTIONS, METHODS & OBJECTS Example 

```js 
I* The scr i pt is placed i nside an immediately invoked function expression
which helps prot ect the scope of variab les *I
-(function() {
II PART ONE : CREATE HOTEL OBJECT AND WRITE OUT THE OFFER DETAILS
II Create a hotel obj ect using object l i t eral syntax
var hotel = {
name: 'Park',
roomRate: 240, II Amount in dollars
discount : 15, II Percentage di scount
offerPrice: function() {
var offerRate = this .roomRate * ((100 - this .discount) I 100);
return offerRate;
II Wr ite out the hotel name, standard rate, and the special rate
var hotel Name, roomRate, specialRate; II Declare variables
hotelName = document .getElementByid('hotelName');
roomRate = document.getElementByid('roomRate');
specialRate = document .getElementByld('specialRate');
II Get el ement s
hotelName.textContent = hotel .name; II Write hotel name
roomRate.textContent = '$ ' + hotel . roomRate .toFixed(2) ; II Write room rate
specialRate .textContent = '$' +hotel .offerPrice(); II Write offer pri ce
```

* Summary 

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