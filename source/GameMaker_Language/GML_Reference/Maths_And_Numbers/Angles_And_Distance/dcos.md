# dcos

In a right angled triangle *cos(val) = Adjacent / Hypotenuse* where val
is one of the three angles. This function will always return a number
between 1 and -1. **NOTE** : This function takes a value in degrees, not
radians.

#### Syntax:

``` gml
dcos(val);
```

|          |                                                                         |                                                 |
|----------|-------------------------------------------------------------------------|-------------------------------------------------|
| Argument | Type                                                                    | Description                                     |
| val      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The angle (in degrees) to return the cosine of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
val = dcos(45);
```

This will set "val" to 0.71.
