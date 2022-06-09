# ds_map_find_previous

This function returns the previous key stored in the DS map *before* the
one specified in the function. This can be useful if your have to
iterate through the DS map looking for something, but should be avoided
if possible as it can be slow. If no such key exists then the function
will return undefined . You should always check this using the [
is_undefined() ](../../Variable_Functions/is_undefined) function.

#### Syntax:

``` gml
ds_map_find_previous(id, key);
```

|          |                                                                                                          |                                      |
|----------|----------------------------------------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                                                     | Description                          |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the map to use.            |
| key      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                 | The key to find the previous one to. |

#### Returns:

``` gml
 Variable

or

 undefined
```

#### Example:

``` gml
var size = ds_map_size(inventory) - 1;
var key = ds_map_find_last(inventory);
for (var i = size; i &amp;gt; 0; i--;)
{
    if (key != "gold")
    {
        key = ds_map_find_previous(inventory, key);
    }
    else break;
}
```

The above code creates some temporary variables and then gets the ds_map
size and finds the last key as stored by the computer in the map. It
then uses a for loop to iterate back through the ds_map looking for the
key value "gold". If it finds it, it breaks out the loop.
