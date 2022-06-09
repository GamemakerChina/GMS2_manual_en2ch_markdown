# timeline_size

With this function you can get the total number of active moments for a
timeline (an "active" moment is one which has code or GML Visual added
to it). This can be handy when creating dynamic timelines using the [
timeline_moment_add_script() ](timeline_moment_add_script) and [
timeline_moment_clear() ](timeline_moment_clear) functions, as you
can check to see if a given timeline has the correct number of active
moments or none at all.

#### Syntax:

``` gml
timeline_size(ind);
```

|          |                                                                    |                                                     |
|----------|--------------------------------------------------------------------|-----------------------------------------------------|
| Argument | Type                                                               | Description                                         |
| ind      |  [Timeline Asset](../../../../../The_Asset_Editors/Timelines)  | The index of the timeline get the information from. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if timeline_size(global.tl) == 0
{
    timeline_moment_add_script(global.tl, room_speed + irandom(room_speed), spawn_enemy);
}
```

The above code check the given timeline size, and if it returns 0 (ie:
the timeline has no active moments) it will add a script function to be
used at a random moment within the timeline indexed in the global
variable "tl".
