# Movement

In any game, movement and position are of paramount importance and so
GameMaker has a complete selection of functions to deal with every
situation. The two main ways of moving an instance is to either set the
actual position or to set a speed/direction vector, and this can be done
either using the built in variables instance variables or to use
specific movement functions. Both of these options are explained in the
sections listed below: The following variables are all included "built
in" to every instance and can be read and modified to change different
behaviours when the instance is moving (they will affect the speed and
direction vectors):

-   [direction](../../Asset_Management/Instances/Instance_Variables/direction)
-   [friction](../../Asset_Management/Instances/Instance_Variables/friction)
-   [gravity](../../Asset_Management/Instances/Instance_Variables/gravity)
-   [gravity_direction](../../Asset_Management/Instances/Instance_Variables/gravity_direction)
-   [hspeed](../../Asset_Management/Instances/Instance_Variables/hspeed)
-   [vspeed](../../Asset_Management/Instances/Instance_Variables/vspeed)
-   [speed](../../Asset_Management/Instances/Instance_Variables/speed)

Other than those variables mentioned above you can also set the instance
position directly using the following:

-   [x](../../Asset_Management/Instances/Instance_Variables/x)
-   [y](../../Asset_Management/Instances/Instance_Variables/y)
-   [xprevious](../../Asset_Management/Instances/Instance_Variables/xprevious)
-   [yprevious](../../Asset_Management/Instances/Instance_Variables/yprevious)
-   [xstart](../../Asset_Management/Instances/Instance_Variables/xstart)
-   [ystart](../../Asset_Management/Instances/Instance_Variables/ystart)

The following functions can all be used to move an instance in some way,
with some affecting the speed/direction vectors and others affecting the
actual x/y position within the room directly:

-   [motion_add](motion_add)
-   [motion_set](motion_set)
-   [move_towards_point](move_towards_point)
-   [move_bounce_all](move_bounce_all)
-   [move_bounce_solid](move_bounce_solid)
-   [move_contact_all](move_contact_all)
-   [move_contact_solid](move_contact_solid)
-   [move_outside_all](move_outside_all)
-   [move_outside_solid](move_outside_solid)
-   [move_random](move_random)
-   [move_snap](move_snap)
-   [move_wrap](move_wrap)
-   [place_snapped](place_snapped)
