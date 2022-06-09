# arccos

Returns the inverse cosine of x, in that if cos(val)=n , arccos(n)=val ,
and the resulting number will be between pi and 0. **NOTE** :This will
only accept a number between -1 and 1 (anything else will throw an
error). **NOTE** : This function takes a value in radians, not degrees.

#### Syntax:

``` gml
arccos(x)
```

|          |                                                                         |                                                         |
|----------|-------------------------------------------------------------------------|---------------------------------------------------------|
| Argument | Type                                                                    | Description                                             |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The angle (in radians) to return the inverse cosine of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
val = arccos(0);
```

This will set val to pi/2.
