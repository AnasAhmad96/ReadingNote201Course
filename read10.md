# 201 Course

![web developer](http://coderoo.com.au/blog/wp-content/uploads/2018/02/web.jpg)

----

| number      | subject |
| ----------- | ----------- |
| 1   |Ch. 10, “Error Handling & Debugging”|

----

# Error Handling & Debugging

|  PREPARE      | EXECUTE |
| ----------- | ----------- |
| • The new scope is created|• Now it can assign values to variables|
|• Variables, functions, and arguments are created |• Reference functions and run their code|
|• The value of the this keyword is determined|• Execute statements|

----

* UNDERSTANDING
SCOPE

> In the interpreter, each execution context has its own va ri ables object.
It holds the variables, functions, and parameters available within it.
Each execution context can also access its parent's v a ri ables object.
Functions in JavaScript are said to have lexical scope.
They are linked to the object they were defined within.
So, for each execution context, the scope is the
current execution context's variables object, plus the
variables object for each parent execution context.
Imagine that each function is a nesting doll.
The children can ask the parents for information in
their variables. But the parents cannot get variables
from their children. Each child will get the same
answer from the same parent.

* UNDERSTANDING ERRORS

> If a JavaScript statement generates an error, then it throws an exception.
At that point, the interpreter stops and looks for exception-handling code.
If you are anticipating that something in your code
may cause an error, you can use a set of statements
to handle the error (you meet them on p480).
This is important because if the error is not handled,
the script will just stop processing and the user will
not know why. So exception-handling code should
inform users when there is a problem.
Whenever the interpreter comes across an error,
it will look for error-handling code. In the diagram
below, the code has the same structure as the code
you saw in the diagrams at the start of the chapter.
The statement at step 1 uses the function in step 2,
which in turn uses the function in step 3. Imagine
that there has been an error at step 3.

* ERROR OBJECTS

> Error objects can help you find where your mistakes are
and browsers have tools to help you read them.

```html
Syntax Error
SYNTAX IS NOT CORRECT
This is caused by incorrect use of the rules of the
language. It is often the result of a simple typo.
MISMATCHING OR UNCLOSED QUOTES
document .write ("Howdyl );
SyntaxError: Unexp ec t ed EOF
MISSING CLOSING BRACKET
document .getElementByid('page' I
SyntaxErr or : Expected token ' ) '
MISSING COMMA IN ARRAY
Would be same for missing] at the end
var l ist = ['Item 1', 'Item 2 ' l 'rtem 3'];
SyntaxError: Expected token ']'
MALFORMED PROPERTY NAME
It has a space but is not surrounded by quote marks
user = { f i rstl name: "Ben", lastName: "Lee"};
Synt axError: Expected an identifier but
found 'name ' instead
```

* HOW TO DEAL WITH
ERRORS

> Now that you know what an error is and how the browser treats them,
there are two things you can do with the errors.
1: DEBUG THE SCRIPT TO FIX ERRORS
If you come across an error while writing a script
(or when someone reports a bug), you will need to
debug the code, track down the source of the error,
and fix it.
You will find that the developer tools available in
every major modern browser will help you with
this task. In this chapter, you will learn about the
developer tools in Chrome and Firefox. (The tools in
Chrome are identical to those in Opera.)
IE and Safari also have their own tools (but there is
not space to cover them all).
@ ERROR HANDLING & DEBUGGING
>> 2: HANDLE ERRORS GRACEFULLY
You can handle errors gracefully using try, catch,
throw, and f i na 1 ly statement s.
Sometimes, an error may occur in the script for a
reason beyond your control. For example, you might
request data from a third party, and their server
may not respond. In such cases, it is particularly
important to write error-handling code.
In the latter part of the chapter, you will learn how to
gracefully check whether something will work, and
offer an alternative option if it fails.

* A DEBUGGING
WORKFLOW

> Debugging is about deduction: eliminating potential causes of an error.
Here is a workflow for techniques you will meet over the next 20 pages.
Try to narrow down where the problem might be, then look for clues.
WHERE IS THE PROBLEM?
First, should try to can narrow down the area where
the problem seems to be. In a long script, this is
especially important.

1. Look at the error message, it tells you:
• The relevant script that caused the problem.
• The line number where it became a problem for
the interpreter. (As you will see, the cause of
the error may be earlier in a script; but this is the
point at which the script could not continue.)
• The type of error (although the underlying cause
of the error may be different).
2. Check how far the script is running.
Use tools to write messages to the console to tell
how far your script has executed.
3. Use breakpoints where things are going wrong.
They let you pause execution and inspect the va lues
that are stored in variables.
If you are stuck on an error, many programmers
suggest that you try to describe the situation (talking
out loud) to another programmer. Explain what
should be happening and where the error appears
to be happening. This seems to be an effective way
of finding errors in all programming languages. (If
nobody else is available, try describing it to yourself.)
WHAT EXACTLY IS THE PROBLEM?
Once you think that you might know the rough area
in which your problem is located, you can then try to
find the actual line of code that is causing the error.
1. When you have set breakpoints, you can see if the
variables around them have the values you would
expect them to. If not, look earlier in the script.
2. Break down I break out parts of the code to test
smaller pieces of the functionality.
• Write values of variables into the console.
• Calrfunctions from the console to check if they
are returning what you would expect them to.
• Check if objects exist and have the methods I
properties that you think they do.
3. Check the number of parameters for a function, or
the number of items in an array.
And be prepared to repeat the whole process if the
above solved one error just to uncover another ...
If the problem is hard to find, it is easy to lose track
of what you have and have not tested. Therefore,
when you start debugging, keep notes of what you
have tested and what the result was. No matter
how stressful the circumstances are, if you can,
stay calm and methodical, the problem will feel less
overwhelming and you will solve it faster.

* BROWSER DEV TOOLS &
JAVASCRIPT CONSOLE

> The JavaScript console will tell you when there is a problem with a script,
where to look for the problem, and what kind of issue it seems to be.
>> These two pages show instructions for opening the
console in all of the main browsers (but the rest of
this chapter will focus on Chrome and Firefox).
Browser manufacturers occasionally change how
to access these tools. If they are not where stated,
search the browser help files for "console."

CHROME/ OPERA
On a PC, press the F12 key or:

1. Go to the options menu (or three line menu icon)
2. Select Toots or More tools.
3. Select JavaScript Console or Developer Tools
On a Mac press Alt + Cmd + J. Or:
4. Go to the View menu.
5. Select Developer.
6. Open the JavaScript Console or Developer Tools
option and select Console.

* HOW TO LOOK AT ERRORS
IN CHROME

> The console will show you when there is an
error in your JavaScript. It also displays the line
where it became a problem for the interpreter.

1. The Console option is selected.
2. The type of error and the error
message are shown in red.
3. The file name and the line
number are shown on the
right-hand side of the console.

* HOW TO LOOK AT ERRORS
IN FIREFOX

1. The Console option is selected.
2. Only the JavaScript and
Logging options need to be
turned on. The Net, CSS, and
Security options show other
information.

----

* LOGGING DATA
TO THE CONSOLE

```js
console.log('And we\'re off ... ');
var $form, width, height, area ;
$form = $('#calculator');
II Indicates script is running
$('form i nput[type="text"]').on( ' blur ' , function() { II When input l oses focus
console . log('You entered ', this.value); II Write va l ue to con sole
} ) ; .
$(' #calculator').on('submit', function(e)
e.preventDefault();
~ console.log('Clicked submit . . . ') ;
width = $('#width').val();
© console.log('Width ' +width} ;
height= $('#height').val();
~ console.log( 'Height ', height);
area = width * height;
@ console. log(area);
$form.append('<p> ' +area+ ' <Ip>')
} ) ;
II When the user clicks submit
II Prevent the form submitting
II Indicate but ton was cl i cked
II Write width to con sol e
II Write height to console
II Wri te area to console
```

* MORE CONSOLE METHODS

> To differentiate between the
types of messages you write
to the console, you can use
three different methods. They
use various colors and icons to
distinguish them.

1. con so 1 e. info() can be used
for general information
2. consol e.warn() can be used
for warnings
3. console .er ror () can be used
to hold errors

```js
console.info('And we\'re off ... ' );
var $form, width, height, area;
$form = $('#calculator ' ) ;
$( ' form input[type="text"]').on('blur', function()
console .warn( ' You entered ', this .value);
} ) ;
$(' #calculator') .on('submi t', function(e) {
e.preventDefault();
wid t h = $('#width').val ();
height= $('#height').val();
area = width * height;
~ console.error(area);
$form.append( '<p class="result">' + area + '<I p>');
} ) ;
```

* GROUPING MESSAGES

> 1. If you want to write a set of
related data to the console, you
can use the console. group ()
method to group the messages
together. You can then expand
and contract the results.
It has one parameter; the name
that you want to use for the
group of messages. You can
then expand and collapse the
contents by cl icking next to the
group's name as shown below.
> 2. When you have finished
writing out the results for the
group, to indicate the end of the
group the console .groupEnd ()
method is used.

```js
var $form = $('#calculator');
$form.on('submit', function(e)
e.preventDefault();
con so 1e .1 og ('Cl i eked submit. . . ') ;
var width, height, area;
width= $('#width') .val();
height= $(' #height') .val();
area = width * height;
CI) console .group( ' Area calculations');
console .i nfo('Width ' , width);
console .info( 'Height ', height);
consol e. l og(area); cY console.groupEnd();
$form.append( ' <p>' +area+ '<I p> ' );
} ) ;
```

* WRITING TABULAR DATA

> In browsers that support it, the
console. table () method lets
you output a table showing:
• objects
• arrays that contain other
objects or arrays
clO/ js/ console-table. j s
The example below shows data
from the contacts object. It
displays the city, telephone
number, and country. It is
particularly helpful when the
data is coming from a third party.
The screen shot below shows
the result in Chrome (it looks the
same in Opera). Safari will show
expanding panels. At the time
of writing Firefox and IE did not
support this method.

```js
var contacts = {
"London": {
II Store contact info in an object literal
"Tel": "+44 (0)207 946 0128",
"Country ": "UK"},
"Sydney": {
"Tel" : "+61 (0)2 7010 1212",
"Country": "Australia"},
"New York" : {
"Tel": "+1 (0)1 555 2104",
"Country": "USA"}
G) console.table(contacts); II Write data to console
var city, contactDetails;
contactDetails = '';
II De~lare variabl es for page
II Hold details wr itten to page
$.each(contacts , function(city, contacts) { II Loop t hrough data to
contactDetails += city+ ': ' +contacts.Tel + '<br I>' ;
} ) ;
$( ' h2').after('<p>' + contactDetails + '<Ip>'); II Add data to the page
```

* WRITING ON A CONDITION

> Using the console. assert()
method, you can test if a
condition is met, and write to the
console only if the expression
evaluates to false.
JAVASCRIPT

> 1. Below, when users leave an
input, the code checks to see if
they entered a value that is 10
or higher. If not, it will write a
message to the screen.
> 2. The second check looks to
see if the calculated area is a
numeric value. If not, then the
user must have entered a value
that was not a number.

```js var $fonn, width, height, area;
$form= $('#calculator');
$('form input[type="text"] ' ) . on('bl ur', function() {
2. The second check looks to
see if the calculated area is a
numeric value. If not, then the
user must have entered a value
that was not a number.
clO/ js/ console-assert .js
II The message only shows if user has entered number less than 10
CD console.assert(this.value > 10, 'User entered less than 10');
} ) ;
$('#calculator') .on('submit', function(e)
e.preventDefault();
console.log('Clicked submit ... ');
width= $( '#width').val();
height= $('#height').val() ;
area = width * height;
II The message on ly shows if user has not entered a number
~ console.assert($.isNumeric(area), 'User entered non-numeric value');
$form.append('<p>' +area+ '<I p>');
} ) ;
```

* HANDLING EXCEPTIONS

> If you know your code might fail, use try, catch, and finally.
Each one is given its own code block.

```js
try {
II Try to execute this code
catch (exception) {
II If there is an exception, run this code
fina ll y {
II This always gets executed
```

-----

* summary
  
* vIf you understand execution contexts (which have two
stages) and stacks, you are more likely to find the error
in your code.
* Debugging is the process of finding errors. It involves a
process of deduction.
* The console helps narrow down the area in which the
error is located, so you can try to find the exact error.
* JavaScript has 7 different types of errors. Each creates
its own error object, which can tell you its line number
and gives a description of the error.
* If you know that you may get an error, you can handle
it gracefully using the try, catch, finally statements.
Use them to give your users helpful feedback.

----

@AnasAhmad
