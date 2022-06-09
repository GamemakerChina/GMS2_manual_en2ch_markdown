# layer_get_depth

You can use this function to get the *depth* value associated with a
given layer. You supply the layer ID (which you get when you create the
layer using [ layer_create() ](layer_create) ) or the layer name (as
a string - this will have a performance impact) and the function will
return that layers depth as a real number. Note that depth is defined as
being higher the "further away" from the camera and lower the "closer"
to the camera, so if you have three layers with depths -100, 0, 100, the
layers will draw in the order 100, 0, -100, so that the "top" layer (ie,
the closest to the camera view and so drawn over everything else) will
be the layer with the -100 depth. The following image shows a schematic
of how depth works for layers:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Rooms/Layer_Depths.png)  
Note that if you supply an invalid layer ID value you will get an error.

#### Syntax:

``` gml
layer_get_depth(layer_id)
```

|          |                                                                                                                                                                                                                  |                                                                                      |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                                                          |
| layer_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to get the depth of (or the layer name as a string) |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if layer_get_depth(global.temp_layer) != -100
{
    layer_destroy(global.temp_layer);
    global.temp_layer = layer_create(-100);
}
```

The above code checks the depth of a layer ID stored in a global
variable and if it is not -100 it destroys the layer and re-creates it
at the depth of -100.
