# is_nan

This function returns whether a given variable is NaN (not a number) or
not, returning true if it is, and false if it is not.

#### Syntax:

``` gml
is_nan(n);
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
if is_nan(global.value)
{
    show_debug_message("Value is not a number");
}
```

The above code checks the global variable "value" to see if it is a
number or not and shows a debug message if it isn't.
