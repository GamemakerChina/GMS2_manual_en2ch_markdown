# vertex_format_add_texcoord

Tell GameMaker to accept texture position data (u and v) as part of the
new vertex format being created.

#### Syntax:

``` gml
vertex_format_add_texcoord();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
vertex_format_begin();
vertex_format_add_texcoord();
vertex_format_add_position_3d();
my_format = vertex_format_end();
```

The above code will create a new vertex format with just texture and
position values and then store the format id in the variable
"my_format".
