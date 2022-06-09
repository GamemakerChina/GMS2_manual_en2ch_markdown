# surface_set_target_ext

This function is for use with the [Shader
Functions](../../Asset_Management/Shaders/Shaders) and sets the MRT
(0 - 3) for native level shaders (DX9, DX11, OpenGL). **NOTE** : When
working with surfaces there is the possibility that they can cease to
exist at any time due to them being stored in texture memory. You should
**ALWAYS** check that a surface exists using [ surface_exists()
](surface_exists) before referencing them directly.

#### Syntax:

``` gml
surface_set_target_ext(index, surface_id);
```

|            |                                                                                                     |                                               |
|------------|-----------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Argument   | Type                                                                                                | Description                                   |
| index      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The render target index to use (from 0 to 3). |
| surface_id |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The ID of the surface to use.                 |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
surface_set_target_ext(0, surf);
```

The above code will set the render target 0 to the surface ID indexed in
the variable "surf".
