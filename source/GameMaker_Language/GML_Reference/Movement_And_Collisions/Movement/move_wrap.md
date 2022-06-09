# move_wrap

This function will automatically "wrap" an instance that has left the
room on either the horizontal or vertical (or both) axis. You can
specify a margin outside the edges of the room for this to occur, and
when the instance has travelled outside of that margin GameMaker will
automatically wrap it back into the room at the other side. Note that
the instance must have a speed for wrapping to work, because the
direction of wrapping is based on the direction of the motion.

#### Syntax:

``` gml
move_wrap(hor, vert, margin);
```

|          |                                                                            |                                                                               |
|----------|----------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                                   |
| hor      |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether to wrap horizontally (true) or not (false).                           |
| vert     |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether to wrap vertically (true) or not (false).                             |
| margin   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | How far outside the room, in pixels, the object must be to initiate wrapping. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
move_wrap(true, false, sprite_width);
```

This will make the instance wrap horizontally but not vertically, when
it is over its own sprite width outside of the room.
