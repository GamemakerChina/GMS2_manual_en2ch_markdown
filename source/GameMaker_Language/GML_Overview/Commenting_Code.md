# Commenting Code

When working in collaboration with other people, when dealing with a
large project, or even just for your own reference and debugging,
leaving comments in your event code and scripts is very important. In
GameMaker you have various mechanisms to help you leave notes and
comments about code sections and even whole blocks of code that can be
seen in the event list of the object that you are currently editing. In
this way you can leave notes to yourself and to your colleagues, or to
explain a particularly tricky piece of code, or even just leave a
reminder about what something does, or what you want something to do in
the future. To leave a simple one-line comment, the first thing you can
do is use ** // ** before the text. For example:

``` gml
//initialize variables
sr = 10;
hp = 100;
```

You may also leave multi-line comments, to give credit, to omit a
complete section of code for debugging, or even to leave notes about how
you want to change the code in the future. For that you can use ** /\*
... \*/ ** like this:

``` gml
/*
Setup GIF Variables to initial values (these can be edited so you don't need to use the setter functions all the time if you are always using the same values)

IMPORTANT! Please see the individual "set" scripts for more extensive information about each of the different variables.
*/

frame_num = 30;
frame_steps = 5;
frame_width = 256;
frame_height = 256;
frame_quality = gifcam_quality_high;
```

Apart from comments you can also use special \#region tags to mark a
section of code for **Code Folding** , and each region can contain a
comment. How this works is that you add a \#region tag - along with any
comment text - to the top of a section of code and then add a
corresponding \#endregion tag to the bottom of the section and then you
can "fold" the code, ie: hide it away so you can cut down on the number
of lines of code visible in the editor at any one time:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Overview/editor_scripts_coderegion.gif)  
The actual code looks something like this:

``` gml
#region This is an example region

width = sprite_get_width(sprite);
height = sprite_get_height(sprite);
xoff = sprite_get_xoffset(sprite);
yoff = sprite_get_yoffset(sprite);

#endregion Further comment here if required
```

Finally, it's worth mentioning that when working with events in the
[Object Editor](../../The_Asset_Editors/Objects) , you can use a
special " description " comment at the start of the event to say what
the general contents of the event are, and this will show in the Object
Editor events window. This should go on the very first line of the code
editor, and is formatted as follows:

``` gml
/// @description &amp;lt;This Is An Event Description&amp;gt;
```

This will now be shown in the event window, eg:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Overview/Event_Comment.png)  
Note that you can define a default comment to be created for all events
from the [Object Editor
Preferences](../../Setting_Up_And_Version_Information/IDE_Preferences/Object_Editor_Preferences)
. Finally, if you are writing [script functions](Script_Functions)
and want to have some control over how they are treated by the IDE (ie:
have auto-complete or show the script parameters) then you should be
writing your comments using JSDoc notation as explained
[here](../../The_Asset_Editors/Code_Editor_Properties/JSDoc_Script_Comments)
.
