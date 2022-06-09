# layer_get_element_layer

You can use this function to get the *Layer ID* that the given element
is on. You supply the unique element ID value (for example, as returned
by the function that created the element or from the room editor) and
the function will return the unique ID of the layer that the element is
found on. If the element ID given is not a valid one, then the function
will return -1.

#### Syntax:

``` gml
layer_get_element_layer(element_id)
```

|            |                                                                                                                                                    |                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| Argument   | Type                                                                                                                                               | Description                                            |
| element_id |  [Layer Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_all_elements)  | The unique ID value of the element to get the layer of |

#### Returns:

``` gml
 Layer ID

or -1 (if the element is invalid)
```

#### Example:

``` gml
element = layer_get_element_layer(asset_1);
```

The above code gets layer ID for the element with the ID stored in the
variable "asset_1" and stores it in a variable.
