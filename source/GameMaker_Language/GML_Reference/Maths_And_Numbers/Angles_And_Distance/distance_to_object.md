# distance_to_object

This function calculates the distance from the edge of the bounding box
of the calling instance to the nearest edge of the nearest instance of
the object specified. The object can be an object index or a specific
instance ID as well as the
[*keyword*](../../../GML_Overview/Instance_Keywords) **other** , and
the distance is returned in pixels. Note that if either of the objects
have no sprite or no mask defined, the results will be incorrect.

#### **Syntax:**

``` gml
distance_to_object(obj);
```

|          |                                                                                                                                                                                         |                          |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| Argument | Type                                                                                                                                                                                    | Description              |
| obj      |  [Object Asset](../../../../../The_Asset_Editors/Objects) or [Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)    | The object to check for. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if (distance_to_object(obj_Player) &amp;lt; range)
{
    canshoot = true;
}
```

The above code will check for the distance to the player object and if
it is less than the value stored in the variable "range" the variable
"canshoot" is set to true.
