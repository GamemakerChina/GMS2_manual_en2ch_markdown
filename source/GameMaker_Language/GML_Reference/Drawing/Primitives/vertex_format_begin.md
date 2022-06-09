# vertex_format_begin

Before you can define your new vertex format you must tell GameMaker
that you're doing so using this function. You must call this first, then
define the format values using the appropriate functions, and finally
call [ vertex_format_end() ](vertex_format_end) to finish the
definition and return the new format "handle".

#### Syntax:

``` gml
vertex_format_begin();
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
