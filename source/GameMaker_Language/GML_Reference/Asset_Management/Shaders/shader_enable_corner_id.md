# shader_enable_corner_id

With this function you can set a global state for all shaders being used
where, when enabled, the shader "steals" 2 bits from the input colour
values. The first is from the lower bit of the red colour value, and the
second is from the lower bit of the blue colour value. These values can
get then be recovered in the shader to work out which vertex you
are dealing with (ie: which corner).

#### Syntax:

``` gml
shader_enable_corner_id(enable);
```

|          |                                                                            |                                                         |
|----------|----------------------------------------------------------------------------|---------------------------------------------------------|
| Argument | Type                                                                       | Description                                             |
| enable   |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Enable ( true ) or disable ( false ) this function.     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
shader_enable_corner_id(true);
```

The above code will enable the use of colour bits for the corner id for
all shaders.
