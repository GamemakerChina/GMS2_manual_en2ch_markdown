# layer_background_index

This function can be used to set the image index of the background
sprite which has multiple sub-images. You give the background element ID
(which you get when you create a background element using [
layer_background_create() ](layer_background_create) or when you use
the function [ layer_background_get_id() ](layer_background_get_id)
), and then set the image index to use. If you set a value outside of
the range of sub-images, then the image index will loop around.

#### Syntax:

``` gml
layer_background_index(background_element_id, image_index);
```

|                       |                                                                                                                                                    |                                                         |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Argument              | Type                                                                                                                                               | Description                                             |
| background_element_id |  [Background Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Background_Layers/layer_background_get_id)  | The unique ID value of the background element to change |
| index                 |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                          | The image index to use for the background               |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var lay_id = layer_get_id("Background_trees");
var back_id = layer_background_get_id(lay_id);
layer_background_index(back_id, 1);
```

The above code will get the layer ID for the layer named
"Background_trees" and then use that to get the ID of the background
element on that layer. This ID is then used to change the element image
index.
