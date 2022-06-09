# buffer_get_surface

With this function you can write information from a surface to a given
buffer. The buffer must have been created previously and should be a
1-byte aligned buffer large enough to store data for the surface you are
going to write (if unsure, use a [grow](buffer_create) buffer or see
the example at the bottom of this page). The information for the surface
will always be written to the start of the buffer (regardless of the
seek position) but you can choose an offset value (in bytes) to move the
write position from the start of the buffer. Note that the function
writes each pixel of the surface to the buffer using an **RGBA**
formatting on the Windows target, but on other targets it may be
different depending on the OS or even the device. **NOTE** : This
function has changed from the GameMaker update 2.3.1 onward. Previous
versions used the constant buffer_surface_copy , which is now
deprecated.

#### Syntax:

``` gml
buffer_get_surface(buffer, surface, offset);
```

|          |                                                                                                  |                                   |
|----------|--------------------------------------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                                                             | Description                       |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)             | The index of the buffer to use.   |
| surface  |  [Surface ID](../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The index of the surface to use.  |
| offset   |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The data offset value (in bytes). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
buffer = buffer_create(surf_width * surf_height * 4, buffer_fixed, 0);
buffer_get_surface(buffer, surface, 0);
```

This code will create a fixed-size buffer which has the capacity to
store 4 bytes per pixel (for the R, G, B and A components) based on the
exact size of the surface, and then copy the surface data into it.
