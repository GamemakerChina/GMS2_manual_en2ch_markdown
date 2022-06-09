# gpu_get_state

This function will get the current GPU state, returning it as a [DS
Map](../../Data_Structures/DS_Maps/DS_Maps) . This can then be
manipulated or even saved, and you can return this map to the GPU using
the function [ gpu_set_state() ](gpu_set_state) .

#### Syntax:

``` gml
gpu_get_state();
```

#### Returns:

``` gml
 DS Map ID
```

#### Example:

``` gml
gpu_map = gpu_get_state();
```

The above code stores the current GPU state in a variable.
