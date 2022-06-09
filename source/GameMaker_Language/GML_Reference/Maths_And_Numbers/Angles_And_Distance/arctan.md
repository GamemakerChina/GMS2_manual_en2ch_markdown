# arctan

Returns the inverse tangent of x. This will accept any number as, unlike
[tan()](tan) , arctan() asymptotes are on the y axis so it just
means you'll never get returned a number greater than pi/2 or less than
-pi/2. **NOTE** : This function takes a value in radians, not degrees.

#### Syntax:

``` gml
arctan(x);
```

|          |                                                                         |                                                          |
|----------|-------------------------------------------------------------------------|----------------------------------------------------------|
| Argument | Type                                                                    | Description                                              |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The angle (in radians) to return the inverse tangent of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
val = arctan( 0 );
```

This will set val to 0.
