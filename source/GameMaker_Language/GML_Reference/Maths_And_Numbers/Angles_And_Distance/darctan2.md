# darctan2

This function returns the inverse tangent of an angle y/x, where y =
Opposite side of triangle and x = Adjacent side of triangle . Unlike [
darctan() ](darctan) the function darctan2() is valid for all angles
and so may be used to convert a vector to an angle without risking
division by zero, and it also returns a result in the correct quadrant.
**NOTE** : The value returned is in degrees, not radians.

#### Syntax:

``` gml
darctan2(y, x);
```

|          |                                                                         |                                |
|----------|-------------------------------------------------------------------------|--------------------------------|
| Argument | Type                                                                    | Description                    |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate to calculate. |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate to calculate. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
val = darctan2(1, 1);
```

This will set "val" to the correct angle.
