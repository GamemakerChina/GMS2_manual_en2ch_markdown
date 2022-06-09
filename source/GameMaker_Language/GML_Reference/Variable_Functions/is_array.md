# is_array

This function can be used to check and see if a variable holds an array
(it will return true ) or not (in which case it will return false ).

#### Syntax:

``` gml
is_array(n);
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
if is_array(a)
{
    a = -1;
}
```

The above code checks a variable to see if it is an array, and if the
function returns true , the array is deleted by setting the variable to
-1.
