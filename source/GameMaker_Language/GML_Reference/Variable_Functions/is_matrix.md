# is_matrix

This function returns whether a given variable refers to a matrix or
not. In some cases you want to check and see what data type a variable
holds in GameMaker and that's when you would use this function. It
returns true or false depending on whether the value is a matrix or not.

#### Syntax:

``` gml
is_matrix(n);
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
if !is_matrix(val)
{
    show_debug_message("Not a valid matrix!");
}
```

The above code checks the variable "val" to see if it contains a matrix
and if it is not then it shows a message in the debug console.
