# tan

In a right angled triangle *tan(val) = Opposite / Adjacent* where val is
one of the three angles. ** NOTE ** This function takes a value in
radians not degrees. **NOTE** : Pi/2, (3 pi/2), -pi/2 and a vast number
of other values will error with this function due to their returning
infinity, a graph representation of this would produce asymptotes at
these values.

#### Syntax:

``` gml
tan(val);
```

|          |                                                                         |                                                  |
|----------|-------------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                                    | Description                                      |
| val      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The angle (in radians) to return the tangent of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
val = tan( pi );
```

This will set val to 0.
