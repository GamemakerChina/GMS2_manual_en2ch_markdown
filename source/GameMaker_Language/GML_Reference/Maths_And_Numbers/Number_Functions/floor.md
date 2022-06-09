# floor

Returns the floor of n, that is, n rounded down to an integer. This is
similar to the [ round() ](round) function, but it only rounds
*down* , no matter what the decimal value, so floor(5.99999) will return
5, as will floor(5.2) , floor(5.6457) etc...

#### Syntax:

``` gml
floor(n);
```

|          |                                                                         |                      |
|----------|-------------------------------------------------------------------------|----------------------|
| Argument | Type                                                                    | Description          |
| n        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The number to floor. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
val = floor( 3.9 );
```

This will set val to 3.
