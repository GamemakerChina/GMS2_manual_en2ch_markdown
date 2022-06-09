# instance_number

With this function you can find out how many active instances of the
specified object exists in the room. When checking using this function,
if the object is a **parent** , then *all child objects will also be
included in the return value* , and also note that those instances which
have been deactivated with the [instance
deactivate](Deactivating_Instances/Deactivating_Instances) functions
will *not* be included in this check.

#### Syntax:

``` gml
instance_number(obj);
```

|          |                                                                |                                                 |
|----------|----------------------------------------------------------------|-------------------------------------------------|
| Argument | Type                                                           | Description                                     |
| obj      |  [Object Asset](../../../../../The_Asset_Editors/Objects)  | The object to total the number of instances of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if instance_number(object_index) &amp;lt; 50
{
    instance_create_layer(random(room_width), random(room_height), "Instances", object_index);
}
```

The above code will check the number of instances that are created form
the same object as the current instance and then if there are less than
50, create another one at a random position within the room.
