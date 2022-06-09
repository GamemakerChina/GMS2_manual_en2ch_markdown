# is_method

This function can be used to check and see if a variable is a method
variable (it will return true ) or not (in which case it will return
false ).

#### Syntax:

``` gml
is_method(n);
```

|          |                                                                                   |                        |
|----------|-----------------------------------------------------------------------------------|------------------------|
| Argument | Type                                                                              | Description            |
| n        |  [Variable](../../../../GameMaker_Language/GML_Overview/Data_Types#variable)  | The variable to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if is_method(get_vec)
{
    show_debug_message("Method variable!");
}
```

The above code checks a variable to see if it is a method, and if the
function returns true , then a debug message is output to the console.
