# is_ptr

This function returns whether a given variable is a pointer or not. In
some cases you want to check and see what data type a variable holds in
GameMaker and that's when you would use this function. It returns true
or false depending on whether the value is a pointer or not.

#### Syntax:

``` gml
is_ptr(n);
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
if !is_ptr(val)
{
    show_debug_message("Not a valid texture!");
}
```

The above code checks the variable "val" to see if it contains a pointer
and if it is not then it shows a message in the debug console.
