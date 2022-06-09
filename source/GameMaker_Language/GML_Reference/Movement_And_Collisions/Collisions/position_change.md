# position_change

This function will check a position for a collision with *any instances*
at the given point, and if there is one, it will change **all**
instances in collision to be instances of the chosen object. You can set
the "perf" argument to true which will force GameMaker to perform the
**Destroy** and **Clean Up** events of the found instance as well as the
**Create** event of the new instance, or false to not perform any of
these events. Please note, that if you choose not to perform the
Destroy, Clean Up and Create events, any instance created that uses a
variable normally defined in the create event will crash the game as
that variable will no longer exist.

#### Syntax:

``` gml
position_change(x, y, obj, perf);
```

|          |                                                                            |                                                                          |
|----------|----------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                              |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The x coordinate of where to change colliding instances.                 |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The y coordinate of where to change colliding instances.                 |
| obj      |  [Object Asset](../../../../../The_Asset_Editors/Objects)              | The new object the calling object will change into.                      |
| perf     |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether to perform that new object's Create event (true) or not (false). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
position_change(200, 200, obj_Bird, true);
```

This will change all instances colliding at point (200,200) into an
instance of "obj_Bird", performing "obj_Bird"s Create event for each of
them in the process.
