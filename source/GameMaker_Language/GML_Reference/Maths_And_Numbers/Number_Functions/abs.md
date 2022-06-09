# abs

This function returns the absolute value of the input argument, so if
it's a positive value then it will remain the same, but if it's negative
it will be multiplied by -1 to make it positive.

#### **Syntax:**

``` gml
abs(val)
```

|          |                                                                         |                              |
|----------|-------------------------------------------------------------------------|------------------------------|
| Argument | Type                                                                    | Description                  |
| val      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The number to turn absolute. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
x += abs (x - mouse_x)
```

This will add an amount equal to the absolute value of the current x
position of the instance and the mouse x position.
