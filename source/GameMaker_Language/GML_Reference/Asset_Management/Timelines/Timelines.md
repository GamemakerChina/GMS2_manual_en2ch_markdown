# Timelines

Timelines are a powerful mechanism for controlling events in your game,
and are based on "moments", where a "moment" is simply a single game
step. These timelines are generally created from the **Asset Browser**
using the [Timeline Editor](../../../../The_Asset_Editors/Timelines)
in a similar way to an object, ie: you create a timeline, then in each
moment that you require it to perform an action you add some code or a
GML Visual icon for it to perform. Once created, you can then stop,
start, and manipulate timelines through code. You can even modify
individual moments by defining a [script
function](../../../GML_Overview/Script_Functions) and adding it into
the timeline dynamically from a controller object (for example), making
this a very powerful and versatile tool when creating your games. The
following functions are for adding and manipulating Timelines from
within your game:

-   [timeline_exists](timeline_exists)
-   [timeline_get_name](timeline_get_name)
-   [timeline_add](timeline_add)
-   [timeline_delete](timeline_delete)
-   [timeline_moment_add_script](timeline_moment_add_script)
-   [timeline_moment_clear](timeline_moment_clear)
-   [timeline_clear](timeline_clear)
-   [timeline_size](timeline_size)
-   [timeline_max_moment](timeline_max_moment)

The following variables are "built in" to all instances to make working
with Timelines easier and give you control over them:

-   [timeline_index](timeline_index)
-   [timeline_running](timeline_running)
-   [timeline_speed](timeline_speed)
-   [timeline_position](timeline_position)
-   [timeline_loop](timeline_loop)

Note that you can find further information on instance variables here:
[Instance
Variables](../Instances/Instance_Variables/Instance_Variables) .
