# Instance Variables

When you create a new object, it will come with certain variables
already initialised with default values. These variables we call
**instance variables** , since they will be created for every instance
you place of the object in your game rooms, and once an instance is
created the values of these variables are unique to that instance and
*only* that instance. Some of these variables you will use a lot, like x
and y , while others are required less depending on what you want to do,
but in general they are very useful and where possible you should be
looking to use them rather than creating your own custom variables. Most
instance variables can be set as well as read, permitting you to change
the properties and behaviour of an instance simply by tweaking the value
of a certain variable - you can prevent an instance from drawing, for
example, by simply setting the visible built-in variable to false .
Below you can find the different variables that are initialised for all
instances of all objects in your game. IMPORTANT If an instance is in a
[sequence](../../../../../The_Asset_Editors/Sequences) then some of
these variables - like image_xscale / image_yscale / image_angle / x / y
 - will be overwritten when the sequence updates each step after
starting to be played.

## General Variables

These variables deal with general instance properties:

-   [id](id)
-   [visible](visible)
-   [solid](solid)
-   [persistent](persistent)
-   [depth](depth)
-   [layer](layer)
-   [alarm](alarm)

## Movement And Position

These variables deal with the instance position and movement:

-   [direction](direction)
-   [friction](friction)
-   [gravity](gravity)
-   [gravity_direction](gravity_direction)
-   [hspeed](hspeed)
-   [vspeed](vspeed)
-   [speed](speed)
-   [xstart](xstart)
-   [ystart](ystart)
-   [x](x)
-   [y](y)
-   [xprevious](xprevious)
-   [yprevious](yprevious)

## Object Properties

The following variable holds the unique index ID of the object that the
instance was created from:

-   [object_index](../../Objects/object_index)

## Sprite Properties

These variables are all related to the sprite assigned to the instance
and can be used to change what is drawn and how:

-   [sprite_index](../../Sprites/Sprite_Instance_Variables/sprite_index)
-   [sprite_width](../../Sprites/Sprite_Instance_Variables/sprite_width)
-   [sprite_height](../../Sprites/Sprite_Instance_Variables/sprite_height)
-   [sprite_xoffset](../../Sprites/Sprite_Instance_Variables/sprite_xoffset)
-   [sprite_yoffset](../../Sprites/Sprite_Instance_Variables/sprite_yoffset)
-   [image_alpha](../../Sprites/Sprite_Instance_Variables/image_alpha)
-   [image_angle](../../Sprites/Sprite_Instance_Variables/image_angle)
-   [image_blend](../../Sprites/Sprite_Instance_Variables/image_blend)
-   [image_index](../../Sprites/Sprite_Instance_Variables/image_index)
-   [image_number](../../Sprites/Sprite_Instance_Variables/image_number)
-   [image_speed](../../Sprites/Sprite_Instance_Variables/image_speed)
-   [image_xscale](../../Sprites/Sprite_Instance_Variables/image_xscale)
-   [image_yscale](../../Sprites/Sprite_Instance_Variables/image_yscale)

## Mask And Bounding Box

These variables deal with the collision mask:

-   [mask_index](../../Sprites/Sprite_Instance_Variables/mask_index)
-   [bbox_bottom](../../Sprites/Sprite_Instance_Variables/bbox_bottom)
-   [bbox_left](../../Sprites/Sprite_Instance_Variables/bbox_left)
-   [bbox_right](../../Sprites/Sprite_Instance_Variables/bbox_right)
-   [bbox_top](../../Sprites/Sprite_Instance_Variables/bbox_top)

## Paths

These variables are related to paths and how the instance interacts with
one, if assigned:

-   [path_index](../../Paths/Path_Variables/path_index)
-   [path_position](../../Paths/Path_Variables/path_position)
-   [path_positionprevious](../../Paths/Path_Variables/path_positionprevious)
-   [path_speed](../../Paths/Path_Variables/path_speed)
-   [path_scale](../../Paths/Path_Variables/path_scale)
-   [path_orientation](../../Paths/Path_Variables/path_orientation)
-   [path_endaction](../../Paths/Path_Variables/path_endaction)

## Timelines

These variables are for setting an instance to use a timeline:

-   [timeline_index](../../Timelines/timeline_index)
-   [timeline_running](../../Timelines/timeline_running)
-   [timeline_speed](../../Timelines/timeline_speed)
-   [timeline_position](../../Timelines/timeline_position)
-   [timeline_loop](../../Timelines/timeline_loop)

## Sequences

The following variables store information regarding the Sequence that
may be controlling the instance at any given time:

-   [in_sequence](../../Sequences/in_sequence)
-   [sequence_instance](../../Sequences/sequence_instance)

## Physics

There are a great number of built in variables for use with the physics
functions of GameMaker , and so to keep things clearer, they can be
found in the section of the manual that covers everything related to the
physics simulation:

-   [Physics](../../../Physics/Physics)
