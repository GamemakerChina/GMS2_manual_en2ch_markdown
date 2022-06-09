# degtorad

In GM all the trigonometric functions work in radians, but most people
work in degrees and this means that to convert your degrees into radians
you need to use this function. For example, degtorad(180) returns
3.14159265 radians. This function translates degrees into radians using
the formula:

``` gml
angle_radians = angle_degrees * pi / 180
```

#### Syntax:

``` gml
degtorad(deg);
```

|          |                                                                         |                         |
|----------|-------------------------------------------------------------------------|-------------------------|
| Argument | Type                                                                    | Description             |
| deg      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The degrees to convert. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
val = degtorad(90);
```

This will set val to pi/2.
