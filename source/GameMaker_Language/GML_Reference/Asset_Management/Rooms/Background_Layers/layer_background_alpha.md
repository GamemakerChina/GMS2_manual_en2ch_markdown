# layer_background_alpha

This function controls the alpha (transparency) of the background
sprite. You give the background element ID (which you get when you
create a background element using [ layer_background_create()
](layer_background_create) or when you use the function [
layer_background_get_id() ](layer_background_get_id) ), and then set
the alpha value to use. Alpha can be between 0 (fully transparent) and 1
(fully opaque) with the default alpha value for the background element
being 1. Note that if the layer the background element has been assigned
to is not visible - or the element itself has been made invisible - you
will not see any difference with this function until the layer or
element has been made visible again.

#### Syntax:

``` gml
layer_background_alpha(background_element_id, alpha);
```

|                       |                                                                                                                                                    |                                                             |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Argument              | Type                                                                                                                                               | Description                                                 |
| background_element_id |  [Background Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Background_Layers/layer_background_get_id)  | The unique ID value of the background element to change     |
| alpha                 |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                          | The alpha for background sprite, from 0 to 1 (default is 1) |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var lay_id = layer_get_id("Background_sky"); var back_id = layer_background_get_id(lay_id); layer_background_alpha(back_id, random(1));
```

The above code gets the ID value of the background assigned to the layer
"Background_sky" and then sets its alpha to a random value between 0 and
1.
