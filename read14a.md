
![web developer](http://coderoo.com.au/blog/wp-content/uploads/2018/02/web.jpg)

----

| number | subject                                            |
| ------ | -------------------------------------------------- |
| 1      | Transforms                                         |
| 2      | Transitions & Animations                           |
| 3      | 8 simple CSS3 transitions that will wow your users |
| 4      | 6 Buttons animated                                 |
| 5      | CSS3 Animations: Keyframes                         |
| 6      | 404                                                |
| 7      | Pure CSS Bounce Animation                          |

----

# Transforms

With CSS3 came new ways to position and alter elements. Now general layout techniques can be revisited with alternative ways to size, position, and change elements. All of these new techniques are made possible by the transform property.
The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.
Within this lesson we’ll take a look at both two-dimensional and three-dimensional transforms. Generally speaking, browser support for the transform property isn’t great, but it is getting better every day. For the best support vendor prefixes are encouraged, however you may need to download the nightly version of Chrome to see all of these transforms in action.

* Transform Syntax

> The actual syntax for the transform property is quite simple, including the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses.

```css
div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
```

* 2D Transforms

> Elements may be distorted, or transformed, on both a two-dimensional plane or a three-dimensional plane. Two-dimensional transforms work on the x and y axes, known as horizontal and vertical axes. Three-dimensional transforms work on both the x and y axes, as well as the z axis. These three-dimensional transforms help define not only the length and width of an element, but also the depth. We’ll start by discussing how to transform elements on a two-dimensional plane, and then work our way into three-dimensional transforms.

```html
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
```

```css
.box-1 {
  transform: rotate(20deg);
}
.box-2 {
  transform: rotate(-55deg);
}
```

* Combining Transforms

> It is common for multiple transforms to be used at once, rotating and scaling the size of an element at the same time for example. In this event multiple transforms can be combined together. To combine transforms, list the transform values within the transform property one after the other without the use of commas.
Using multiple transform declarations will not work, as each declaration will overwrite the one above it. The behavior in that case would be the same as if you were to set the height of an element numerous times.

```html
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
```

```css
.box-1 {
  transform: rotate(25deg) scale(.75);
}
.box-2 {
  transform: skew(10deg, 20deg) translateX(20px);
}
```

* Transform Origin

> As previously mentioned, the default transform origin is the dead center of an element, both 50% horizontally and 50% vertically. To change this default origin position the transform-origin property may be used.
The transform-origin property can accept one or two values. When only one value is specified, that value is used for both the horizontal and vertical axes. If two values are specified, the first is used for the horizontal axis and the second is used for the vertical axis.
Individually the values are treated like that of a background image position, using either a length or keyword value. That said, 0 0 is the same value as top left, and 100% 100% is the same value as bottom right. More specific values can also be set, for example 20px 50px would set the origin to 20 pixels across and 50 pixels down the element.

```html
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
<figure class="box-3">Box 3</figure>
<figure class="box-4">Box 3</figure>
```

```css
.box-1 {
  transform: rotate(15deg);
  transform-origin: 0 0;
}
.box-2 {
  transform: scale(.5);
  transform-origin: 100% 100%;
}
.box-3 {
  transform: skewX(20deg);
  transform-origin: top left;
}
.box-4 {
  transform: scale(.75) translate(-10px, -10px);
  transform-origin: 20px 50px;
}
```

* Perspective

> In order for three-dimensional transforms to work the elements need a perspective from which to transform. The perspective for each element can be thought of as a vanishing point, similar to that which can be seen in three-dimensional drawings.
The perspective of an element can be set in two different ways. One way includes using the perspective value within the transform property on individual elements, while the other includes using the perspective property on the parent element residing over child elements being transformed.
Using the perspective value within the transform property works great for transforming one element from a single, unique perspective. When you want to transform a group of elements all with the same perspective, or vanishing point, apply the perspective property to their parent element.
The example below shows a handful of elements all transformed using their individual perspectives with the perspective value.

```html
<figure class="box">Box 1</figure>
<figure class="box">Box 2</figure>
<figure class="box">Box 3</figure>
```

```css
.box {
  transform: perspective(200px) rotateX(45deg);
}
```

* 3D Transforms

> So far we’ve discussed how to rotate an object either clockwise or counterclockwise on a flat plane. With three-dimensional transforms we can rotate an element around any axes. To do so, we use three new transform values, including rotateX, rotateY, and rotateZ.
Using the rotateX value allows you to rotate an element around the x axis, as if it were being bent in half horizontally. Using the rotateY value allows you to rotate an element around the y axis, as if it were being bent in half vertically. Lastly, using the rotateZ value allows an element to be rotated around the z axis.
As with the general rotate value before, positive values will rotate the element around its dedicated axis clockwise, while negative values will rotate the element counterclockwise.

```html
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
<figure class="box-3">Box 3</figure>
```

```css
.box-1 {
  transform: perspective(200px) rotateX(45deg);
}
.box-2 {
  transform: perspective(200px) rotateY(45deg);
}
.box-3 {
  transform: perspective(200px) rotateZ(45deg);
}
```

* Transform Style

> On occasion three-dimensional transforms will be applied on an element that is nested within a parent element which is also being transformed. In this event, the nested, transformed elements will not appear in their own three-dimensional space. To allow nested elements to transform in their own three-dimensional plane use the transform-style property with the preserve-3d value.
The transform-style property needs to be placed on the parent element, above any nested transforms. The preserve-3d value allows the transformed children elements to appear in their own three-dimensional plane while the flat value forces the transformed children elements to lie flat on the two-dimensional plane.

```html
<div class="rotate three-d">
  <figure class="box">Box 1</figure>
</div>
<div class="rotate">
  <figure class="box">Box 2</figure>
</div>
```

```css
.rotate {
  transform: perspective(200px) rotateY(45deg);
}
.three-d {
  transform-style: preserve-3d;
}
.box {
  transform: rotateX(15deg) translateZ(20px);
  transform-origin: 0 0;
}
```

* Backface Visibility

> When working with three-dimensional transforms, elements will occasionally be transformed in a way that causes them to face away from the screen. This may be caused by setting the rotateY(180deg) value for example. By default these elements are shown from the back. So if you prefer not to see these elements at all, set the backface-visibility property to hidden, and you will hide the element whenever it is facing away from the screen.
The other value to backface-visibility is visible which is the default value, always displaying an element, no matter which direction it faces.
In the demonstration below notice how the second box isn’t displayed because backface-visibility: hidden; declaration has been set. The backface-visibility property takes even more significance when using animations.

```html
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
```

```css
.box-1 {
  transform: rotateY(180deg);
}
.box-2 {
  backface-visibility: hidden;
  transform: rotateY(180deg);
}
```

-----

# Transitions & Animations

One evolution with CSS3 was the ability to write behaviors for transitions and animations. Front end developers have been asking for the ability to design these interactions within HTML and CSS, without the use of JavaScript or Flash, for years. Now their wish has come true.

With CSS3 transitions you have the potential to alter the appearance and behavior of an element whenever a state change occurs, such as when it is hovered over, focused on, active, or targeted.

Animations within CSS3 allow the appearance and behavior of an element to be altered in multiple keyframes. Transitions provide a change from one state to another, while animations can set multiple points of transition upon different keyframes.

```css
.box {
  background: #2db34a;
  transition-property: background;
  transition-duration: 1s;
  transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29;
}
```

* Transitional Properties

> It is important to note, not all properties may be transitioned, only properties that have an identifiable halfway point. Colors, font sizes, and the alike may be transitioned from one value to another as they have recognizable values in-between one another. The display property, for example, may not be transitioned as it does not have any midpoint. A handful of the more popular transitional properties include the following.

* background-color
* background-position
* border-color
* border-width
* border-spacing
* bottom
* crop
* color
* clip
* font-size
* font-weight
* height
* line-height
* letter-spacing
* left
* margin
* max-height
* max-width
* opacity
* min-width
* min-height
* outline-color
* outline-offset
* outline-width
* text-indent
* right
* padding
* text-shadow
* top
* vertical-align
* word-spacing
* width
* visibility
* z-index

```css
.box {
  background: #2db34a;
  border-radius: 6px;
  transition-property: background, border-radius;
  transition-duration: .2s, 1s;
  transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29;
  border-radius: 50%;
}
```

```css
button {
  border: 0;
  background: #0087cc;
  border-radius: 4px;
  box-shadow: 0 5px 0 #006599;
  color: #fff;
  cursor: pointer;
  font: inherit;
  margin: 0;
  outline: 0;
  padding: 12px 20px;
  transition: all .1s linear;
}
button:active {
  box-shadow: 0 2px 0 #006599;
  transform: translateY(3px);
}
```

------

# 8 simple CSS3 transitions that will wow your users

* Fade in

> Having things fade in is a fairly common request from clients. It’s a great way to emphasize functionality or draw attention to a call to action.
Fade in effects are coded in two steps: first, you set the initial state; next, you set the change, for example on hover:

```css
.fade
{
        opacity:0.5;
}
.fade:hover
{
        opacity:1;
}
```

* Change color

> Animating a change of color used to be unbelievably complex, with all kinds of math involved in calculating separate RGB values and then recombining them. Now, we just set the div’s class to “color” and specify the color we want in our CSS:

```css
.color:hover
{
        background:#53a7ea;
}
```

* Grow & Shrink

> To grow an element, you used to have to use its width and height, or its padding. But now we can use CSS3’s transform to enlarge.
Set your div’s class to “grow” and then add this code to your style block:

```css
.grow:hover
{
        -webkit-transform: scale(1.3);
        -ms-transform: scale(1.3);
        transform: scale(1.3);
}
```

* Rotate elements

> CSS transforms have a number of different uses, and one of the best is transforming the rotation of an element. Give your div the class “rotate” and add the following to your CSS:

```css
.rotate:hover
{
        -webkit-transform: rotateZ(-30deg);
        -ms-transform: rotateZ(-30deg);
        transform: rotateZ(-30deg);
}
```

* Square to circle

A really popular effect at the moment is transitioning a square element into a round one, and vice versa. With CSS, it’s a simple effect to achieve, we just transition the border-radius property.
Give your div the class “circle” and add this CSS to your styles:

```css
.circle:hover
{
        border-radius:50%;
}
```

* 3D shadow

> 3D shadows were frowned upon for a year or so, because they weren’t seen as compatible with flat design, which is of course nonsense, they work fantastically well to give a user feedback on their interactions and work with flat, or fake 3D interfaces.
This effect is achieved by adding a box shadow, and then moving the element on the x axis using the transform and translate properties so that it appears to grow out of the screen.
Give your div the class “threed” and then add the following code to your CSS:

```css
.threed:hover
{
        box-shadow:
                1px 1px #53a7ea,
                2px 2px #53a7ea,
                3px 3px #53a7ea;
        -webkit-transform: translateX(-3px);
        transform: translateX(-3px);
}
```

* Swing

> Not all elements use the transition property. We can also create highly complex animations using @keyframes, animation and animation-iteration.
In this case, we’ll first define a CSS animation in your styles. You’ll notice that due to implementation issues, we need to use @-webkit-keyframes as well as @keyframes (yes, Internet Explorer really is better than Chrome, in this respect at least).

```css
@-webkit-keyframes swing
{
    15%
    {
        -webkit-transform: translateX(5px);
        transform: translateX(5px);
    }
    30%
    {
        -webkit-transform: translateX(-5px);
       transform: translateX(-5px);
    } 
    50%
    {
        -webkit-transform: translateX(3px);
        transform: translateX(3px);
    }
    65%
    {
        -webkit-transform: translateX(-3px);
        transform: translateX(-3px);
    }
    80%
    {
        -webkit-transform: translateX(2px);
        transform: translateX(2px);
    }
    100%
    {
        -webkit-transform: translateX(0);
        transform: translateX(0);
    }
}
@keyframes swing
{
    15%
    {
        -webkit-transform: translateX(5px);
        transform: translateX(5px);
    }
    30%
    {
        -webkit-transform: translateX(-5px);
        transform: translateX(-5px);
    }
    50%
    {
        -webkit-transform: translateX(3px);
        transform: translateX(3px);
    }
    65%
    {
        -webkit-transform: translateX(-3px);
        transform: translateX(-3px);
    }
    80%
    {
        -webkit-transform: translateX(2px);
        transform: translateX(2px);
    }
    100%
    {
        -webkit-transform: translateX(0);
        transform: translateX(0);
    }
}
```

* Inset border

> One of the hottest button styles right now is the ghost button; a button with no background and a heavy border. We can of course add a border to an element simply, but that will change the element’s position. We could fix that problem using box sizing, but a far simpler solution is the transition in a border using an inset box shadow.
Give your div the class “border” and add the following CSS to your styles:

```css
.border:hover
{
        box-shadow: inset 0 0 0 25px #53a7ea;
}
```

----

# 6 Buttons animated

```html
<div class="group">
  <button class="blam">Blam</button>
  <button style="-webkit-animation-delay: .3s;animation-delay: .3s;" class="syke">Syke</button>
  <button style="-webkit-animation-delay: .6s;animation-delay: .6s;" class="later">Later</button>
</div>
```

```css
@import url(https://fonts.googleapis.com/css?family=Droid+Sans:700);
  *{
   margin: 0;
   padding: 0;
   box-sizing: border-box;
   transition: all .1s;
  }
  body{
  background-color: #424242;
   font-family: 'Droid Sans', sans-serif;
  }
  .group{
   text-align: center;
   margin: 20px auto;
  }
  .group button{
   margin-top: 10px;
  }
  button{
/*   box-sizing: border-box;*/
   background: NONE;
   border: none;
   outline: none;
   border-radius: 3px;
   padding: 15px 70px;
   color:white;
   text-transform: uppercase;
   font-weight: 700;
   text-shadow: 0 1px 3px rgba(0, 0, 0, 0.41);
   box-shadow: 0 3px 0 0 #383838;
   border:3px solid transparent;
   
  
   animation: pulse 1s linear infinite alternate;
   -webkit-animation: pulse 1s linear infinite alternate;
  }
  .active,
  button:active{
   background-image: linear-gradient(rgba(0,0,0,.1) 13%, transparent 13%,transparent);
   box-shadow: 0 1px 0 0 #383838;
   color: rgba(0, 0, 0,.45);
   text-shadow: none;
   
   
   -webkit-animation-play-state: paused; 
     animation-play-state: paused;
  }
  button:focus,
  button:hover{
   -webkit-animation-play-state: paused; 
     animation-play-state: paused;
  }
  
  
  .blam:focus,
  .blam:hover{
   background-color:#0097bd;
  }
  .blam{
   background-color:#00bff0;
   border-color: #00bff0;
  }
  
  .syke:focus,
  .syke:hover{
   background-color:#ad4e4e;
  }
  .syke{
   background-color:#e06464;
   border-color:#e06464;
  }
  
  .later:focus,
  .later:hover{
   background-color:#7c8b8f;
  }
  .later{
   background-color:#a8bdc2;
   border-color:#a8bdc2;
  }
  
  @-webkit-keyframes pulse {
   100% {
    transform: translateY(6.9px); 
   } 
  }

  @keyframes pulse {
   100% {
    transform: translateY(6.9px); 
   } 
  }
```

```js
//author: https://dribbble.com/shots/1527712-Buttons
```

 ----

# CSS3 Animations: Keyframes

 ```html
 <h1>CSS3 Animations: Keyframes</h1>


<div class="exampleDiv">
  <div class="ball" style="-webkit-animation: bouncing 2s 15 linear;-moz-animation: bouncing 2s 15 linear;"></div>
</div>


<!-- WhatsHelp.io widget -->
<script type="text/javascript">
    (function () {
        var options = {
            facebook: "220186546416", // Facebook page ID
            company_logo_url: "//storage.whatshelp.io/widget/d2/d2db/d2dbaa07f22d96b7ad8426beb00493d0/20031613_10154783116346417_1007255058190022230_n.png", // URL of company logo (png, jpg, gif)
            greeting_message: "Hello, how may I help you? Just send us a message now to get assistance.", // Text of greeting message
            call_to_action: "Message me", // Call to action
            position: "right", // Position may be 'right' or 'left'
        };
        var proto = document.location.protocol, host = "whatshelp.io", url = proto + "//static." + host;
        var s = document.createElement('script'); s.type = 'text/javascript'; s.async = true; s.src = url + '/widget-send-button/js/init.js';
        s.onload = function () { WhWidgetSendButton.init(host, proto, options); };
        var x = document.getElementsByTagName('script')[0]; x.parentNode.insertBefore(s, x);
    })();
</script>
```

```css
@import url(https://fonts.googleapis.com/css?family=Montserrat:700);
body {
  background-color: #ffcc46;
}

::-webkit-scrollbar {
    width: 8px;
}

::-webkit-scrollbar-thumb {
    background: rgba(0,0,0,0.12);
}

::-webkit-scrollbar-track {
    visibility: hidden;
}

h1 {
  font-family: 'Montserrat', helvetica, arial;
  sans-serif;
  margin: 20px;
}

.exampleDiv {
  height: 200px;
  width: 200px;
  border: 1px solid rgba(0, 0, 0, 0.1);
  float: left;
  margin: 20px;
  text-align: center;
  position: relative;
  background-color: #ffffff;
  border-radius: 4px;
}

.ball {
  position: absolute;
  height: 20px;
  width: 20px;
  border-radius: 10px;
  background-color: #c0392b;
}

@-webkit-keyframes bouncing {
  40%, 70%, 90% {
    bottom: 0;
    -webkit-animation-timing-function: ease-out;
  }
  0% {
    bottom: 200px;
    left: 0;
    -webkit-animation-timing-function: ease-in;
  }
  55% {
    bottom: 50px;
    -webkit-animation-timing-function: ease-in;
  }
  80% {
    bottom: 25px;
    -webkit-animation-timing-function: ease-in;
  }
  95% {
    bottom: 10px;
    -webkit-animation-timing-function: ease-out;
  }
  100% {
    left: 110px;
    bottom: 0;
    -webkit-animation-timing-function: ease-out;
  }
  @-moz-keyframes bouncing {
    40%, 70%, 90% {
      bottom: 0;
      -webkit-animation-timing-function: ease-out;
    }
    0% {
      bottom: 200px;
      left: 0;
      -webkit-animation-timing-function: ease-in;
    }
    55% {
      bottom: 50px;
      -webkit-animation-timing-function: ease-in;
    }
    80% {
      bottom: 25px;
      -webkit-animation-timing-function: ease-in;
    }
    95% {
      bottom: 10px;
      -webkit-animation-timing-function: ease-out;
    }
    100% {
      left: 110px;
      bottom: 0;
      -webkit-animation-timing-function: ease-out;
    }
```

----

# 404

```html
<h1>4</h1>
<h1>0</h1>
<h1>4</h1>
```

```css
body {
  margin:0;
  font-family:sans-serif;
  color:#f25252;
  background:#f7f7f7;
}
h1 {
  font-size:11rem;
  position:absolute;
  transform:translate(-50%,-50%);
  margin:0;
}
h1:nth-of-type(1){
  animation: range 4s infinite;
}
h1:nth-of-type(2){
  left:50%;
  top:50%;
  animation: size 4s infinite;
}
h1:nth-of-type(3){
  animation: range2 4s infinite;
}
@keyframes range {
  0%  {left:42%;top:50%;font-size:11rem;}
  25% {left:50%;top:40%;font-size:4.5rem;}
  50% {left:58%;top:50%;font-size:11rem;}
  75% {left:50%;top:60%;font-size:4.5rem;}
  100%{left:42%;top:50%;font-size:11rem;}
}
@keyframes range2 {
  0%  {left:58%;top:50%;font-size:11rem;}
  25% {left:50%;top:60%;font-size:4.5rem;}
  50% {left:42%;top:50%;font-size:11rem;}
  75% {left:50%;top:40%;font-size:4.5rem;}
  100%{left:58%;top:50%;font-size:11rem;}
}
@keyframes size {
  0%  {font-size:11rem;}
  25% {font-size:26rem;}
  50% {font-size:11rem;}
  75% {font-size:26rem;}
  100%{font-size:11rem;}
}
```

----

@AnasAhmad