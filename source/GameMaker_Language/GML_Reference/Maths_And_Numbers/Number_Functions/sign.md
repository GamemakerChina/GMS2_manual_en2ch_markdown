# sign

This function returns whether a number is positive, negative or neither
and returns 1, -1, 0 respectively. For example - sign(458) will return
1, sign(-5) will return -1 and sign(0) will return 0.

#### Syntax:

``` gml
sign(n);
```

|          |                                                                         |                                |
|----------|-------------------------------------------------------------------------|--------------------------------|
| Argument | Type                                                                    | Description                    |
| n        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The number to get the sign of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
y += sign(y - mouse_y);
```

The above code will add 1, -1 or 0 onto y depending on the result of y -
mouse_y .
