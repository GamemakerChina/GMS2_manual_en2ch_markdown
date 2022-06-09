# object_get_persistent

This function will tell you whether the object you are checking has been
flagged as "persistent" or not. A persistent object is one that will
cause any instances of it to be carried through from room to room unless
they are explicitly destroyed. Please note that this is not an instance
function! So, you can have a persistent object and a non-persistent
instance of the same object and vice-versa. You can set an individual
instances persistent flag using the [ persistent
](../Instances/Instance_Variables/persistent) instance variable.

#### Syntax:

``` gml
object_get_persistent(obj);
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
if (!persistent) &amp;amp;&amp;amp; (object_get_persistent(object_index))
{
    persistent = true;
}
```

The above code will check the instance running it to see if it is
persistent or not as well as check the object index of the instance to
see if it is flagged as persistent or not. If the instance is *not*
persistent yet the object index is flagged as persistent, it will set
"persistent" to true for that instance.
