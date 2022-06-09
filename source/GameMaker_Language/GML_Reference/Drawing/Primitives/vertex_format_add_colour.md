# vertex_format_add_colour

Tell GameMaker to accept colour data as part of the new vertex format
being created.

#### Syntax:

``` gml
vertex_format_add_colour();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
vertex_format_begin(); vertex_format_add_colour();
 vertex_format_add_position();
 my_format = vertex_format_end();
```

The above code will create a new vertex format with just colour and
position values and then store the format id in the variable
"my_format".
