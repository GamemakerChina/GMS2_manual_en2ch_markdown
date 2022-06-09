# radtodeg

Once you have done your calculations using sin, or cos etc... the result
is in radians. This may not always be what you want and so to turn the
radians into degrees we use this function. For example,
radtodeg(sin(180)) will return -45 degrees. This function translates
radians into degrees using the formula:

``` gml
angle_degrees = angle_radians * 180 / pi;
```

#### Syntax:

``` gml
radtodeg(rad);
```

|          |                                                                         |                         |
|----------|-------------------------------------------------------------------------|-------------------------|
| Argument | Type                                                                    | Description             |
| rad      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The radians to convert. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
val = radtodeg( pi );
```

This will set val to 180.
