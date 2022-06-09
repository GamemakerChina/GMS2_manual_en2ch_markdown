# layer_instance_get_instance

This function can be used to get the unique instance ID of the given
instance element. You give the instance *element* ID (see the code
example below for how to get this), and the function will return a real
value that represents the unique [instance
id](../../Instances/Instance_Variables/id) for the element. If the
element is not an instance, the function will return -1.

#### Syntax:

``` gml
layer_instance_get_instance(element_id)
```

|            |                                                                                                                                                       |                                                              |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| Argument   | Type                                                                                                                                                  | Description                                                  |
| element_id |  [Instance Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_all_elements)  | The unique ID value of the instance element to get the ID of |

#### Returns:

``` gml
 Instance ID
```

#### Example:

``` gml
elements = layer_get_all_elements("Instances");
for (var i = 0; i &amp;lt; array_length(elements); i++)
{
     if (layer_get_element_type(elements[i]) == layerelementtype_instance)
     {
         var layerelement = elements[i];
         var inst = layer_instance_get_instance(layerelement);
         inst.x = inst.x + 10;
     }
}
```

The above code will check get all the instance elements on a layer, then
get their unique ID value and use that to move them 10px to the right.
