# lerp

With this function you can find the value that equates to the position
between two other values for a given percentage. So if you do, for
example:

``` gml
lerp(0, 10, 0.5)
```

you would get the return value of 5, which is 50% of the input values.
You can extrapolate using this function too, by supplying a positive or
negative value for the interpolation amount so that doing something
like:

``` gml
lerp(0, 10, 2)
```

will return a value of 20.

#### Syntax:

``` gml
lerp(a, b, amt)
```

|          |                                                                         |                            |
|----------|-------------------------------------------------------------------------|----------------------------|
| Argument | Type                                                                    | Description                |
| a        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The first value.           |
| b        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The second value.          |
| amt      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The amount to interpolate. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
xx = lerp(x, x + hspeed, room_speed); yy = lerp(y, y + vspeed, room_speed);
```

The above code uses the linear interpolation function to predict where
an instance would have moved to after one second of game time.
