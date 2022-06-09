# object_get_physics

This function will tell you whether the object you are checking has been
flagged as "physics enabled"  - in which case it'll return true , - or
not - in which case it will return false .

#### Syntax:

``` gml
object_get_physics(obj);
```

|          |                                                                |                                   |
|----------|----------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                           | Description                       |
| obj      |  [Object Asset](../../../../../The_Asset_Editors/Objects)  | The index of the object to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if object_get_physics(object_index)
{
    phy_active = true;
}
```

The above code will check the instance running it to see if the object
it is created from is physics enabled, and if it is it activates the
physics simulation for the instance.
