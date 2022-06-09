# is_struct

This function checks if the supplied value is a struct. It returns true
if it is, otherwise it returns false . Note that [method
variables](../../GML_Overview/Method_Variables) will also return
true , and [object
instances](../Asset_Management/Instances/Instances) will return
false .

#### Syntax:

``` gml
is_struct(val);
```

|          |                                                                                   |                     |
|----------|-----------------------------------------------------------------------------------|---------------------|
| Argument | Type                                                                              | Description         |
| val      |  [Variable](../../../../GameMaker_Language/GML_Overview/Data_Types#variable)  | The value to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if is_struct(a)
{
    delete(a);
}
```

The above code checks a variable to see if it is a struct, and if the
function returns true , the struct is deleted.
