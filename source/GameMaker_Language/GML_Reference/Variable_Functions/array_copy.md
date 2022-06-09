# array_copy

With this function you can copy all or part of an array into another
array at any position. You need to supply both the source and the
destination arrays (both need to have been created previously), as well
as a position within the source array to copy from and a position within
the destination array to copy to. Finally you need to specify the length
of the array (or the length of the part that you want) to copy. If the
data being copied exceeds the length of the destination array, the array
will be extended to accept the data. This function can also be used for
multi-dimension arrays, as long as you specify which dimension you want
to copy when you supply the array index, following this pattern:

``` gml
// Copy to the first dimension of an array
// from the second dimension of an array
array_copy(item_array, 0, inventory_array[0], 0, len);

// Copy to the third dimension of an array
// from the first dimension of an array
array_copy(item_array[0][0], 0, inventory_array, 0, len);

// etc...
```

#### Syntax:

``` gml
array_copy(dest, dest_index, src, src_index, length);
```

|            |                                                                      |                                                 |
|------------|----------------------------------------------------------------------|-------------------------------------------------|
| Argument   | Type                                                                 | Description                                     |
| dest       |  [Array](../../../../GameMaker_Language/GML_Overview/Arrays)     | The ID of the array to copy to.                 |
| dest_index |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The index within the array to copy to.          |
| src        |  [Array](../../../../GameMaker_Language/GML_Overview/Arrays)     | The ID of the array to copy from.               |
| src_index  |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The index with the array to start copying from. |
| length     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The length (number of array indices) to copy.   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if !array_equals(inventory_array, item_array)
{
    var len = array_length(inventory_array);
    array_copy(item_array, 0, inventory_array, 0, len);
}
```

The above code will check two arrays to see if they hold equivalent
values, and if they do not then the code will copy the entire contents
of the array "inventory_array" into the array "item_array".
