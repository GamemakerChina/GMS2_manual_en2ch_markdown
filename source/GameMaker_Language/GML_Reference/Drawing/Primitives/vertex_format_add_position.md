# vertex_format_add_position

Tell GameMaker to accept 2D positional data (x and y) as part of the new
vertex format being created.

#### Syntax:

``` gml
vertex_format_add_position();
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
