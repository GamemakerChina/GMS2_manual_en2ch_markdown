# object_get_parent

This function will get you the object index of any parent that has been
assigned to the specified object, or else return -100 to show that the
object has no parent assigned to it, or -1 if the object being checked
does not exist. For more information on parents see the section on the
[Object Editor](../../../../The_Asset_Editors/Objects) .

#### Syntax:

``` gml
object_get_parent(obj);
```

|          |                                                                |                                  |
|----------|----------------------------------------------------------------|----------------------------------|
| Argument | Type                                                           | Description                      |
| obj      |  [Object Asset](../../../../../The_Asset_Editors/Objects)  | The index of the object to check |

#### Returns:

``` gml
 Object Asset
```

#### Example:

``` gml
par = object_get_parent(object_index);
```

The above code will get the parent of the object index for the instance
running the code and store the return value in the variable "par".
