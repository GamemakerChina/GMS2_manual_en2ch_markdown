# is_bool

This function returns whether a given variable is a boolean ( true ior
false ) or not. In some cases you want to check and see if a variable in
GameMaker holds a boolean value, and that's when you would use this
function.

#### Syntax:

``` gml
is_bool(n);
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
if is_bool(val)
{
    global.Sound = val;
}
else
{
    global.Sound = true;
}
```

The above code checks the variable "val" to see if it is a real number
and if it is it then uses it to set a global variable.
