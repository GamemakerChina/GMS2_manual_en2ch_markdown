# layer_get_script_begin

You supply the layer ID (which you get when you create the layer using [
layer_create() ](layer_create) ) or the layer name (as a string -
this will have a performance impact) and this function will return the
[script function](../../../../GML_Overview/Script_Functions) index
of the function assigned to run at the beginning of rendering for that
layer, or it will return -1 if no function is assigned. You can assign
script functions to a layer with
[layer_script_begin()](layer_script_begin) and
[layer_script_end()](layer_script_end) .

#### Syntax:

``` gml
layer_get_script_begin(layer_id);
```

|          |                                                                                                                                                                                                                  |                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                                                |
| layer_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to target (or the layer name as a string) |

#### Returns:

``` gml
 Script Function

or -1 (if no function is assigned)
```

#### Example:

``` gml
if layer_get_script_begin(layer) == -1
{
    layer_script_begin(layer, scr_SetShaderValues);
}
```

The above code will check to see if the layer that the instance running
the code has a script function assigned to it and if it doesn't one is
assigned.
