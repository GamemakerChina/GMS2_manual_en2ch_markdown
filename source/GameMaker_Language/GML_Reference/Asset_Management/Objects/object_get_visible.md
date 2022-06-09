# object_get_visible

This function will tell you whether the object you are checking has been
flagged as "visible" (runs its draw event) or not (does not run its draw
event). Please note that this is not an instance function! So, you can
have a visible object and an invisible instance of the same object and
vice-versa. You can set an individual instances visibility using the [
visible ](../Instances/Instance_Variables/visible) instance
variable.

#### Syntax:

``` gml
object_get_visible(obj);
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
if (!visible) &amp;amp;&amp;amp; (object_get_visible(object_index))
{
    visible = true;
}
```

The above code will check the instance running it to see if it is
visible or not as well as check the object index of the instance to see
if it is flagged as visible or not. If the instance is *not* visible yet
the object index is flagged as on, it will set "visible" to true for
that instance.
