# timeline_moment_add_script

With this function you can dynamically add a
[script function](../../../GML_Overview/Script_Functions) to
Timelines at any given "moment" within that time line, where a "moment"
is the equivalent of one game tick (or step). In this way you can create
a new time line using the [ timeline_add() ](timeline_add) function
and add different behaviours at any point, or simply modify a previously
created time line resource with new behaviours. Note that the function
cannot require any additional arguments when using this function, and if
you use it to modify a Timeline asset present in the Asset Browser, then
all instances that use this timeline will be affected, and the change
will last until the end of the game (calling game_restart() will not
reset the change either).

#### Syntax:

``` gml
timeline_moment_add_script(ind, step, script);
```

|          |                                                                                          |                                                          |
|----------|------------------------------------------------------------------------------------------|----------------------------------------------------------|
| Argument | Type                                                                                     | Description                                              |
| ind      |  [Timeline Asset](../../../../../The_Asset_Editors/Timelines)                        | The index of the timeline to add a moment to.            |
| step     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The moment (step) to add to.                             |
| script   |  [Script Function](../../../../../GameMaker_Language/GML_Overview/Script_Functions)  | The index of the script function to add into the moment. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
global.tl = timeline_add();
var i = room_speed * 60;
repeat(3)
{
    timeline_moment_add_script(global.tl, i, choose(Attack_1, Attack_2, Attack_3);
    i += room_speed * 60;
}
```

The above code will create a new time line and store its index in the
variable "global.tl". It will then add three scripts to the time line,
chosen at random, at one minute intervals.
