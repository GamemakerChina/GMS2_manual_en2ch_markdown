# path_endaction

This variable can be used to get or to change the reaction of an
instance when it reaches the end of the current path. Normally you would
set this when you start the path using [ path_start()
](../path_start) but you may wish to change this behaviour depending
on any number of events in your game. The available values are expressed
using the following constants:

|                                                                                                                                           |                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
|  [Path End Action Constant](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Paths/Path_Variables/path_endaction)  |                                                                              |
| Constant                                                                                                                                  | Description                                                                  |
|  path_action_stop                                                                                                                         | Stop the path                                                                |
|  path_action_restart                                                                                                                      | Continue from start position, jumping to the start if the path is not closed |
|  path_action_continue                                                                                                                     | Start the path again from the current position                               |
|  path_action_reverse                                                                                                                      | Reverse the speed of the path (run the path in reverse)                      |

#### Syntax:

``` gml
path_endaction;
```

#### Returns:

``` gml
 Path End Action Constant
```

#### Example:

``` gml
if (path_endaction == path_action_stop)
{
    path_endaction = path_action_reverse;
}
```

The above code will check the path end action and if it's set to stop,
then the end action will be changed to reverse.
