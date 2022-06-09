# object_get_solid

This function will tell you whether the object you are checking has been
flagged as "solid" or not. A solid object generates a special collision
event when using the traditional collision system (ie: the physics world
is off). Please note that this is not an instance function! So, you can
have a solid object and a normal instance of the same object and
vice-versa. You can set an individual instances solid flag using the [
solid ](../Instances/Instance_Variables/solid) instance variable.

#### Syntax:

``` gml
object_get_solid(obj);
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
if (!solid) &amp;amp;&amp;amp; (object_get_solid(object_index))
{
    solid = true;
}
```

The above code will check the instance running it to see if it is solid
or not as well as check the object index of the instance to see if it is
flagged as solid or not. If the instance is *not* solid yet the object
index is flagged as solid, it will set "solid" to true for that
instance.
