# draw_highscore

This simple function will draw the current list of internally stored
high scores using the currently set font, colour and alpha values within
the specified rectangle. You provide the coordinates for the upper left
corner and lower right corner of the rectangular area to draw the text,
and GameMaker will take care of the rest, with spacing and position
being done automatically.

#### Syntax:

``` gml
draw_highscore( x1, y1, x2, y2 );
```

|          |                                                                         |                                                            |
|----------|-------------------------------------------------------------------------|------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the left of the highscore rectangle.   |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the top of the highscore rectangle.    |
| x2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the right of the highscore rectangle.  |
| y2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the bottom of the highscore rectangle. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_highscore(100, 100, room_width - 100, room_height - 100);
```

This would draw the highscore table in a rectangle in the middle of the
room with a 100px border.
