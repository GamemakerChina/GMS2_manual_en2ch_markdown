# is_infinity

This function returns whether a given variable is infinity (an infinite
number) or not, returning true if it is, and false if it is not.

#### Syntax:

``` gml
is_infinity(n);
```

|          |                                                                                   |                        |
|----------|-----------------------------------------------------------------------------------|------------------------|
| Argument | Type                                                                              | Description            |
| n        |  [Variable](../../../../GameMaker_Language/GML_Overview/Data_Types#variable)  | The argument to check. |

#### Returns:

``` gml
 Boolean
```

#### **Example:**

``` gml
if is_infinity(global.value)
{
    show_debug_message("Value is infinite!");
}
```

The above code checks the global variable "value" to see if it is
infinite or not and shows a debug message if it is.
