# gpu_set_state

This function will set the current GPU state using the passed-in [DS
Map](../../Data_Structures/DS_Maps/DS_Maps) . The supplied map can
be created using the function [gpu_get_state()](gpu_get_state) .

#### Syntax:

``` gml
gpu_set_state(ds_map);
```

|          |                                                                                                          |                                      |
|----------|----------------------------------------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                                                     | Description                          |
| ds_map   |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The GPU state to set as a DS Map .   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
gpu_set_state(gpu_map);
```

The above code sets the GPU state using the map supplied in the variable
"gpu_map".
