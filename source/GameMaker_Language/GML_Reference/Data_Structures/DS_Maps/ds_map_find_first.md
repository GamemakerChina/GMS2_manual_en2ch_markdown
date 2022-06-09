# ds_map_find_first

This function returns the first key stored in the DS map. **This is not
the first key in the order you added them!** DS maps are not stored in a
linear form, for that use [DS list](../DS_Lists/DS_Lists) , so all
this does is find the first key as stored by the computer. This can be
useful if your have to iterate through the DS map looking for something,
but should be avoided if possible as it can be slow. Note that this
function will return undefined if the given DS map is empty.

#### Syntax:

``` gml
ds_map_find_first(id);
```

|          |                                                                                                          |                           |
|----------|----------------------------------------------------------------------------------------------------------|---------------------------|
| Argument | Type                                                                                                     | Description               |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the map to use. |

#### Returns:

``` gml
 Variable

or

 undefined
```

#### Example:

``` gml
var size = ds_map_size(inventory) ;
var key = ds_map_find_first(inventory);
for (var i = 0; i &amp;lt; size; i++;)
{
    if key != "gold"
    {
        key = ds_map_find_next(inventory, key);
    }
    else break;
}
```

The above code creates some temporary variables and then gets the DS
map size and finds the first key as stored by the computer in the map.
It then uses a for loop to iterate through the DS map looking for the
key value "gold". If it finds it, it breaks out the loop.
