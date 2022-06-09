# bool

This function will attempt to convert a given value into a boolean data
type, where the value will be returned as true if it is greater than or
equal to 0.5, and false otherwise.

#### Syntax:

``` gml
bool(n);
```

|          |                                                                      |                       |
|----------|----------------------------------------------------------------------|-----------------------|
| Argument | Type                                                                 | Description           |
| n        |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The value to convert. |

#### Returns:

``` gml
 Boolean
```

#### **Example:**

``` gml
if !is_bool(val)
{
    val = bool(val);
}
```

The above code checks the variable "val" to see if it is a boolean and
if it is not then it is converted to one.
