# vertex_format_end

This function must be called after defining any new vertex format. It
returns the new format "handle" (index) which must be used in all
further vertex functions that refer to this new format.

#### Syntax:

``` gml
vertex_format_end();
```

#### Returns:

``` gml
 Vertex Format ID
```

#### Example:

``` gml
vertex_format_begin();
vertex_format_add_colour();
vertex_format_add_position();
my_format = vertex_format_end();
```

The above code will create a new vertex format with just colour and
position values and then store the format id in the variable
"my_format".
