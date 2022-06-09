# path_start

A path is created from a series of defining points that are linked
together and then used to plan the movements of an instance. They can be
created with code, *or* in the Path Editor and they are assigned to an
instance to use in the game. You would then use this function to tell
your instance which path to follow, what speed to follow the path
(measured in pixels per step), how to behave when it reaches the end of
the path, and whether to follow the *absolute* or *relative* path
position. This last part means that it either starts and follows the
path exactly as you designed and placed it in the [Path
Editor](../../../../The_Asset_Editors/Paths) (absolute), or it
starts and follows the path from the position at which the instance was
created (relative).  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Paths/path_relative_image.png)  
As you can see in the above image, the two instances are following the
same path started with path_start() , but one of the instances is
following the absolute path while the other is following the relative
path. It should be noted that when relative is set to false (absolute)
the instance will "jump" to the start of the path no matter where in the
room it is placed. The constants used to define the behaviour of the
instance when it reaches the end of the path are given [on this
page](Path_Variables/path_endaction) .

#### Syntax:

``` gml
path_start(path, speed, endaction, absolute);
```

|           |                                                                                                                                        |                                                                                                                                                |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Argument  | Type                                                                                                                                   | Description                                                                                                                                    |
| path      |  [Path Asset](../../../../../The_Asset_Editors/Paths)                                                                              | The path index to start.                                                                                                                       |
| speed     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                 | The speed of which to follow the path in pixels per step, negative meaning going backwards.                                                    |
| endaction |  [Path End Action Constant](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Paths/Path_Variables/path_endaction)  | What to do when the end of the path is reached (see the constants listed above).                                                               |
| absolute  |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                              | Whether the calling instance should follow the absolute path as it is in the editor (true) or a relative path to its current position (false). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
path_start(path, 4, path_action_reverse, 0);
```

This will make the calling instance follow the path indexed in the
variable "path" at a speed of 4 pixels per step. It will follow the path
relative to its own position, and when it reaches the end it will
reverse direction and go back the way it came.
