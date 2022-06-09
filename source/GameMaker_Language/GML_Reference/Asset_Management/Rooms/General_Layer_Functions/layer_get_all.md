# layer_get_all

This function will return an
[array](../../../../GML_Overview/Arrays) populated with the unique
ID values of each layer in the room.

#### Syntax:

``` gml
layer_get_all()
```

#### Returns:

``` gml
 Array

(populated with Layer IDs)
```

#### Example:

``` gml
var a = layer_get_all();
for (var i = 0; i &amp;lt; array_length(a); i++;)
{
    layer_destroy(a[i]);
}
```

The above code retrieves all the layers in a room and adds their ID
values to an array. This array is then parsed to destroy or the room
layers.
