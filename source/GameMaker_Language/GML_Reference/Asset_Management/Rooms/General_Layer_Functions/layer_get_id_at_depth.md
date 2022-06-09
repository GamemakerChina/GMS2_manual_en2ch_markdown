# layer_get_id_at_depth

You can use this function to get the IDs of all layers assigned a
specific depth. You give the depth to check and the function will return
an [array](../../../../GML_Overview/Arrays) with 1 or more entries
depending on whether there are any layers at the given depth or not. If
there are no layers at the given depth then the array will have a single
entry at the \[0\] position with a value of -1, but, if there are layers
at the depth, then an entry will be made in the array for each layer
found - the entry value will be the unique ID value for a layer.

#### Syntax:

``` gml
layer_get_id_at_depth(depth)
```

|          |                                                                            |                                                     |
|----------|----------------------------------------------------------------------------|-----------------------------------------------------|
| Argument | Type                                                                       | Description                                         |
| depth    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The depth to check and retrieve the layer IDs from. |

#### Returns:

``` gml
 Array
```

#### Example:

``` gml
var a = layer_get_id_at_depth(0);
if a[0] != -1
{
    for (var i = 0; i &amp;lt; array_length(a); i++;)
    {
        layer_destroy(a[i]);
    }
}
```

The above code retrieves data about the layers with a depth of 0. A
check is done to see if any layers exist at that depth, and if there are
then the returned array is parsed and each of the found layers is
destroyed.
