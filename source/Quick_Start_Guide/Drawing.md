# Drawing

This section (and the following section on [Movement and
Controls](Movement_And_Controls) ) is aimed at giving you practical
examples of GML or GML Visual to enable you to get started as quickly as
possible making your first game projects. We won't be explaining things
in too much depth as we want you to get started making stuff as quickly
as possible, so we encourage you to explore any links as you go along
and to use the "search" function of the manual to look for additional
information on anything you aren't sure about. In this section we're
going to concentrate on simply drawing information to the screen, both
as text and as images, and also explain a bit more about the different
**Draw Events** , specifically, the main **Draw** event and the **Draw
GUI** event (note that in some of the examples you will be required to
add other events, but we'll explain these as we come to them).  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawEvents.png)  
Before going any further, you might want to make a new project (either
GML or GML Visual) from the [Start
Page](../Introduction/The_Start_Page) , and add (or create) a few
sprites as well as an object or two, as we'll be giving you some code
that you can test using these. Even a white square will work for now as
the sprite for our object! Now, as mentioned in the section on [Objects
And Instances](Objects_And_Instances) , if you don't add a Draw
Event to the object, then GameMaker will default draw, meaning that if
the object has a sprite assigned to it this sprite will be drawn,
complete with any transforms that have been added. What do we mean by
transforms? Well, each object has a number of built-in variable s that
will control how an instance of the object draws its sprite when default
drawing, and you can change these variables as the game runs to change
the way the sprite is drawn. **NOTE** : You can find a list of all the
built in variables that can be used for transforming instance sprites
[here](../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Instance_Variables/Sprite_Instance_Variables)
. GML Visual users have some dedicated actions that affect these
variables, which you can find
[here](../Drag_And_Drop/Drag_And_Drop_Reference/Drawing/Drawing_Actions)
, and you can also use the actual variables themselves along with the
[Get Instance
Variable](../Drag_And_Drop/Drag_And_Drop_Reference/Instance/Get_Instance_Variable)
and [Set Instance
Variable](../Drag_And_Drop/Drag_And_Drop_Reference/Instance/Set_Instance_Variable)
actions. Let's look at some examples: [ Changing Alpha (Transparency)
Changing Alpha (Transparency) ](#) The **alpha** value is what controls
the transparency of what's being drawn, and in GameMaker , you can use
the image_alpha built-in variable to change how transparent the assigned
sprite is. To see how this works, open (or create) an object, assign it
a sprite, and then give the object a **Create Event** . In the Create
Event, simply add the following GML Visual or GML:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_1.png)  

``` gml
var _val = random(1);

image_alpha = _val;
```

Image alpha is calculated as a value from 0 to 1, where 0 is fully
transparent and 1 is fully opaque (by default it's set to 1). So in this
example, all we're doing is setting the image alpha to a random decimal
value from 0 to 1. Place a few instances of this object in a room, and
then click the **Play** button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_PlayGame.png)  
at the top of the IDE. You should see that each instance of the object
draws its sprite with a different transparency, eg:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_1.png)  
[ Changing Colour Blend (Tinting) Changing Colour Blend (Tinting) ](#)
When your object is default drawing a sprite, this sprite is actually
being drawn **blended** (or **tinted** ) with a colour, and this colour
value is stored in the image_blend built-in variable. By default this
colour is white, which essentially means that no colour will be added to
the sprite when it is shown on the screen. However, you can use other
colours to achieve special effects, for example, use red to show the
instance has received some damage. In this example, we're going to blend
different colours with the sprite while a key is pressed and held down,
and so you'll need to open (or create) an object, assign it a sprite,
and then give the object a **Key Down Event** .  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_Add_SpaceKeyPressEvent.png)  
In this Key Down Event, add the following GML Visual or GML:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_2.png)  

``` gml
var _col = choose(c_red, c_green, c_blue, c_yellow, c_fuchsia, c_orange);

image_blend = _col;
```

Place a few instances of this object in a room, and then click the Play
button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_PlayGame.png)  
at the top of the IDE, and test holding down and releasing the *Space*
key. You should see that each instance will change it's colour rapidly
while the key is held down, and stop changing when it is released:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_2.png)  
[ Changing Scale Changing Scale ](#) Another of the properties that we
can change for our sprite is the **scale** value, permitting us to draw
it bigger or smaller whenever we want. Scale is caculated independently
along the X and Y axis by two seperate variables, the image_xscale
variable and the image_yscale variable. By default these are set to 1,
and they act like **multipliers** , so a value of 0.5 would be half
scale and a value of 2 would be double the scale. **IMPORTANT!**
Changing the assigned sprite scale using these variables **will also
change the size of the bounding box to match** , which means that the
collision detection area for the sprite will also scale. In this
example, we're going to use some simple maths to make an instance scale
the sprite up and down in a loop. To start with, open (or create) an
object, assign it a sprite, and then give the object a **Create Event**
. In this event add the following:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_3_1.png)  

``` gml
timer = 0;
```

Now add a **Step Event** to the object with this:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_3_2.png)  

``` gml
timer = timer + 1;

var _val = dsin(timer);

image_xscale = 1 + _val;

image_yscale = 1 + _val;
```

Here we're using the maths function [ dsin()
](../GameMaker_Language/GML_Reference/Maths_And_Numbers/Angles_And_Distance/dsin)
to generate a value between -1 and 1 using the timer variable, and then
applying that to the scale variables. After placing some instances into
a room and pressing the **Play** button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_PlayGame.png)  
, you should see how the instances scale up and down from a scale of 0
to a scale of 2 and then back again.  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_3.gif)  
One last thing... change the " image_yscale " section to " 1 - \_val "
and see what happens! The above examples illustrate just some of the
many ways that you can manipulate the object sprite when GameMaker is
default drawing, but what about if you want to draw more than one thing
for an object? In those cases you need to use the **Draw Event** to
explicitly tell GameMaker what to draw, which is what we'll do in the
following examples. [ Drawing Two (or more) Sprites Together Drawing Two
(or more) Sprites Together ](#) For this example, you'll need two
sprites and one object. Call the sprites " spr_One " and " spr_Two ",
and then set the " spr_One " origin to the center and for " spr_Two "
set its origin to the middle-left:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_4_1.png)  
Assign the first sprite (" spr_One " with the center origin) to the
object you have created and then add a **Create Even** t. In the Create
Event add the following GML Visual or GML:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_4_1.png)  

``` gml
draw_angle = 0;
```

We are going to use this variable to rotate " spr_Two " over time, and
draw it overlayed on the sprite assigned to the object (" spr_One "). To
do this we need to add a **Draw Event** to the object. By doing this we
are telling GameMaker that we want to take over what the instance draws,
which means that our code will include a call to the [ draw_self()
](../GameMaker_Language/GML_Reference/Drawing/Sprites_And_Tiles/draw_self)
function or [**Draw
Self**](../Drag_And_Drop/Drag_And_Drop_Reference/Drawing/Draw_Self)
action. This action simply replicates what the object does when no Draw
Event is present and it is default drawing the assigned sprite. We'll
then draw the second sprite that we want to use as the overlay sprite
that is rotating. The GML Visual and GML looks like this:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_4_2.png)  

``` gml
draw_self();

draw_angle = draw_angle + 0.5;

draw_sprite_ext(spr_Two, 0, x, y, 1, 1, draw_angle, c_red, 1);
```

Add a number of instances of the object into the room editor and then
press the **Play** button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_PlayGame.png)  
at the top of the IDE . If all has gone correctly you should see
something like this now:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_4_2.gif)  
Before we leave this example, let's just tweak it a little bit and
instead of having " spr_Two " simply rotate, we'll make it point towards
the mouse position. For that we need to change the Draw Event GML Visual
or GML to look like this:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_4_3.png)  

``` gml
draw_self();

draw_angle = point_direction(x, y, mouse_x, mouse_y);

draw_sprite_ext(spr_Two, 0, x, y, 1, 1, draw_angle, c_red, 1);
```

Run the project again and this time you'll see something very
different!  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_4_3.gif)  
The sprite now points towards the mouse regardless of where you move it
to! As you can see, layering sprites is a great way to add details to an
object or to have something move independently of the "base" sprite
assigned to the object, and it's a powerful tool that you'll probably
use a lot in your own projects. [ Drawing Things Other Than Sprites
Drawing Things Other Than Sprites ](#) You can draw things in the Draw
Event other than sprites too, like text, or shapes. In this example,
we'll use the GML Visual or GML draw_self() function to draw the object
sprite, but we'll also draw some other stuff, starting with some
**text** . For this example, you'll need a sprite and an object (with
the sprite assigned to it). In the object, first add a **Create Event**
with this GML Visual or GML:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_5_1_1.png)  

``` gml
name = choose("Fred", "Jonas", "Sharon", "Kate", "Frank", "John", "Monica", "Amanda");

number = irandom(100);
```

All this does is tell GameMaker to choose one of the listed names and
assign it to a variable, as well as generate a random number from 0 to
100 for each instance of the object. We want to draw these values to the
screen, and so for that you need to now add a **Draw Event** and in it
add the following GML Visual or GML:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_5_1.png)  

``` gml
draw_self();

draw_set_halign(fa_center);

draw_text(x, y + 32, "My name is " + name);

draw_text(x, y + 48, "My number is " + string(number));
```

You'll notice in the above code that we use the [ string()
](../GameMaker_Language/GML_Reference/Strings/string) function or
[**Number To
String**](../Drag_And_Drop/Drag_And_Drop_Reference/Data_Types/Number_To_String)
action on the "number " variable that we want to draw. This is because
all text has to be made up of *characters* , not values, and so we need
to use this function/action to convert the number value into those
characters that we want to draw. In this case we are taking the random
number we generated and turning it into a "string" of characters that
can be drawn. Also note that we set the text **alignment** . This simply
tells GameMaker where to start drawing the text relative to the given
position, and in this case we want the text to be centered along the
x-axis. Add a number of instances of the object into the room editor and
then press the Play button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_PlayGame.png)  
at the top of the IDE. You should see something like this:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_5_1.png)  
In all the examples so far we've been drawing the sprite assigned to the
instance, but that doesn't always have to be the case. **You can draw
anything you want** in the draw event, regardless of the sprite
assigned. To illustrate this point, we'll change the code that we have
currently by removeing the draw_self() call and replace with a function
to draw a coloured ellipse, like this:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_5_2.png)  

``` gml
draw_ellipse_colour(x - 50, y - 32, x + 50, y + 32, c_fuchsia, c_lime, false);

draw_set_halign(fa_center);

draw_text(x, y + 32, "My name is " + name);

draw_text(x, y + 48, "My number is " + string(number));
```

Run the project again and you should see this:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_5_2.png)  
One important thing to note about this, is that even though we aren't
drawing the assigned sprite, **it will still be used for collision
detection** . So, while you may be drawing one thing, collisions will
still be calculated based on the assigned sprite as if it was placed in
the room along with the instance, even if it's not visible. This is
quite handy actually, as it means you can draw different sprites, but
maintain a single **collision mask** based on the assigned sprite. Also
note that you can still apply the different transforms like X/Y scale,
and collisions will be based on the changed size, even though there is
nothing being drawn to show this.

# The GUI Layer

We mentioned at the top of the page that we'd be talking about the
**Draw GUI Event** as well as the Draw Event, so let's look at that now.
The Draw GUI Event works on something called the **GUI Layer** , which
is a special drawing layer of a fixed width and height that is drawn
over the instances in the room. The great thing about the GUI layer is
that *it doesn't move with the room camera* , so it's the ideal place to
add static GUI items, like scores, healthbars and other information that
your game requires to communicate to the user. You can find out more
information on the GUI layer from the [Draw
Events](../The_Asset_Editors/Object_Properties/Draw_Events) section
of the manual. **NOTE** : Rooms can be larger than the screen size, so
you can have large levels for the player to move around in. This means
that in the Room Editor (or in code) you need to define a **camera**
that follows the action of your game. This is basically a way of setting
up a fixed area of the screen to display different parts of the larger
room based on - for example - the player position in the room, and is
used in a lot of games. Think of the way that the view always follows
the main character in classic games like Mario or Zelda. That's done
with cameras. For more information see the section [Room
Properties](../The_Asset_Editors/Room_Properties/Room_Properties) on
the Room Editor section of the manual. The following examples are all
going to be using the **Draw GUI** event, so you'll need to create an
object and add that event to it. Note that the object doesn't need a
sprite assigned, as we are not wanting to default draw anything, nor do
we need it to detect collisions. Objects like this, that are only
designed for drawing things or controlling certain aspects of the game
are often called **Controller Objects** . Also note that we will be
using the same object for all the examples, so we recommend that you go
through them one after the other (although this is not strictly
necessary).  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawGUIObject.png)  
[ Drawing Text Drawing Text ](#) When drawing to the GUI layer, the
top-left corner is the origin position, and to the right is +X and down
is +Y. This makes positioning text and graphics very easy, as you'll see
in this example. All we're going to do here is draw a value that
represents the player score, so in our object we'll need to add a
**Create Event** to initialise a variable to hold this value, like
this:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_6_1.png)  

``` gml
player_score = 0;
```

We also want to add a **Keyboard Down Event** to the object, as we'll be
using that to increment the score every time you press the Space key.  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_Add_SpaceKeyPressEvent.png)  
In this event add the following:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_6_2.png)  

``` gml
var _val = irandom(100);

player_score = player_score + _val;
```

Finally, let's draw the score value in the Draw GUI event, like this: In
this event add the following:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_6_3.png)  

``` gml
draw_set_halign(fa_left);

draw_set_colour(c_yellow);

draw_text(32, 32, "SCORE:");

draw_set_colour(c_white);

var _str = string(player_score);

draw_text_transformed(32, 48, _str, 2, 2, 0);
```

You'll notice how we've used hard-coded (or fixed) values for the x/y
position of the text to be drawn, since we don't need it to be relative
to any instance as we are drawing to the GUI layer. We've also used the
"set colour" function to change the colour of the text, as well as the
"transformed" fucntion to make the actual score value larger, which
illustrates how you can go about customising text elements in your own
games. Add a single instance of this object to your room now and then
press the **Play** button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_PlayGame.png)  
. When the game runs press and release the key and you should see the
score value increase.  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_6.gif)  
[ Drawing Sprites Drawing Sprites ](#) In this example, we are going to
use the GUI layer to draw some sprites. The most obvious use for this is
to draw the players lives, so lets go ahead and do just that! You'll
need a sprite for this example - which should be about 64x64 pixels -
but it shouldn't be assigned to the object, as we'll be drawing it
ourselves. To start with, we need to add some new variables to the
object in the **Create Event** (if you've done the previous example, add
the following below what's already there):  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_7_1.png)  

``` gml
player_lives = 3;

gui_w = display_get_gui_width();
```

In this code we initialise a variable for the player lives, but we also
create a variable to hold the width of the GUI layer, so that we can
position things correctly relative to the right of the screen. We could
just hardcode a value into the code and use that, but that would mean
that if we make any changes to the size of the room, or if we add
cameras etc... later, then we'd need to go through the code and change
the value everywhere. Using the [ display_get_gui_width()
](../GameMaker_Language/GML_Reference/Cameras_And_Display/display_get_gui_width)
function instead means that we don't need to worry about any future
changes like that as the code will adapt automatically to whatever size
the GUI layer ends up. Next we want to add a **Keyboard Pressed Event**
to the object, as we'll be using that to change the number of lives
every time the Enter key is pressed:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_Add_EnterKeyPressEvent.png)  
In this event add the following:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_7_2.png)  

``` gml
player_lives = player_lives - 1;


if player_lives &amp;lt; 0

{

player_lives = 3;

}
```

Finally, we need to draw the sprites to the display. For this we'll be
using a " for " loop (information using GML
[here](../GameMaker_Language/GML_Overview/Language_Features/for) and
for GML Visual
[here](../Drag_And_Drop/Drag_And_Drop_Reference/Loops/For) ), along
with the GUI width variable to position everything in the top right
corner of the screen. So, add this into the Draw Gui Event (after any
other actions that it may have from previous examples):  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_7_3.png)  

``` gml
for (var i = 0; i &amp;lt; player_lives; i += 1)

{

var _xx = gui_w - 48 - (i * 70);

draw_sprite(spr_Heart, 0, _xx, 48);

}
```

If you haven't already added an instance of this object to a room, go
ahead and add it now (only one!), then press the **Play** button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_PlayGame.png)  
. Once the game is running press the key various times to see the lives
change.  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_7.gif)  
Before you leave this example, you should experiment with the number of
lives and see what happens. At the moment it's set to 3, but change the
Create Event and the Key Pressed event to set the value to 5, or 10...
if you've done everything right, then the code should adapt and draw
them all correctly! [ Drawing A Healthbar Drawing A Healthbar ](#) This
final example covers drawing a healthbar to the GUI layer. There are a
number of ways that this can be done, but GameMaker has a built in
function specifically for doing healthbars, so that's what we'll be
using here, although you can create your own using sprites or shapes
too. To start with, as before, we need to initialise a varaible to hold
the health value, so add the following GML Visual or GML into the
**Create Event** of the object (after any other code that may already be
there):  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_8_1.png)  

``` gml
player_health = 100;
```

We want to use the arrow keys to change the health value up or down
depending on which arrow key is pressed, and we could do that by adding
in two **Keyboard Pressed** events, however it's probably easier to use
a **Step Event** and some code to check for the keys, so go ahead and
add a **Step Event** now with the following GML Visual or GML:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_8_2.png)  

``` gml
if keyboard_check(vk_up)

{

if player_health &amp;lt; 100

{

player_health = player_health + 1;

}

}


if keyboard_check(vk_down)

{

if player_health &amp;gt; 0

{

player_health = player_health - 1;

}

}
```

With that done, we can actually get around to drawing the healthbar,
which is done in the Draw GUI event, adding the following (after
anything else that is already there):  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_DnD_8_3.png)  

``` gml
var _xx = gui_w / 2;

draw_healthbar(_xx - 50, 24, _xx + 50, 40, player_health, c_black, c_red, c_lime, 0, true, true);
```

Add an instance of this object to a room if you haven't already done so
(only one, though!), and then press the **Play** button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_PlayGame.png)  
. Once the game is running press the and keys various times to see the
health change.  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_DrawExample_8.gif)  
We hope that after doing these examples you have a bit more confidence
when using GameMaker and a bit more understanding of how it all works.
The next section will explore how to get these things you've been
drawing to move around the room as well as accept - and respond to -
user input.
