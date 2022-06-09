# vertex_format_add_normal

Tell GameMaker to accept surface normal data (nx, ny and nz) as part of
the new vertex format being created.

#### Syntax:

``` gml
vertex_format_add_normal();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
vertex_format_begin(); vertex_format_add_textcoord();
 vertex_format_add_normal();
 my_format = vertex_format_end();
```

The above code will create a new vertex format with just texture and
surface normal values and then store the format id in the variable
"my_format".
