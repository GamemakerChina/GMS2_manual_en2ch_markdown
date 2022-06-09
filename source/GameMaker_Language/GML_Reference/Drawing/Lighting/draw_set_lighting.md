# draw_set_lighting

This function is used to enable all lighting effects. Default is
disabled ( false ).

#### Syntax:

``` gml
draw_set_lighting(enable);
```

|          |                                                                            |                                                   |
|----------|----------------------------------------------------------------------------|---------------------------------------------------|
| Argument | Type                                                                       | Description                                       |
| enable   |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Enable or disable all lighting ( true or false)   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_set_lighting(true);
draw_light_define_direction(1, 0, 1, 0, c_white);
draw_light_enable(1, true);
```

The above code will enable lighting for the whole scene, then define a
white directional light in the room space, and then finally turn that
light on.
