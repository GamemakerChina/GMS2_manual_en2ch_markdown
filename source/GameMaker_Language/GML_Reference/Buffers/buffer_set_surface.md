# buffer_set_surface

With this function you can write information from a buffer to a given
surface. Both the buffer being read from and the surface being written
to must have been created previously, and you can provide an offset into
the buffer to start reading from. Note that reading will always start at
the beginning of the buffer plus the offset value and *not* at the
current seek position plus the offset value. **NOTE** : This function
has changed from the GameMaker update 2.3.1 onward. Previous versions
used the constant buffer_surface_copy , which is now deprecated.

#### Syntax:

``` gml
buffer_set_surface(buffer, surface, offset);
```

|          |                                                                                                  |                                  |
|----------|--------------------------------------------------------------------------------------------------|----------------------------------|
| Argument | Type                                                                                             | Description                      |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)             | The index of the buffer to use.  |
| surface  |  [Surface ID](../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The index of the surface to use. |
| offset   |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The data offset value.           |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
buffer_set_surface(buff, application_surface, 0);
```

The above code will copy all the data stored in the buffer indexed in
the variable "buff" to the application surface with no offset.
