# ds_map_destroy

DS maps take up space in memory, which is allocated to them when they
are created. This means that you also need to free this memory when the
DS map is not needed to prevent errors, memory leaks and loss of
performance when running your game. This function does just that. Note
that destroying a map will de-reference any data structures stored in
the map giving a memory leak, so you would need to go through the map
and destroy all data structure items manually before destroying it to
prevent this. The only time this is not required is when you have
flagged any items in the map as a [DS list](../DS_Lists/DS_Lists) or
as another [DS map](DS_Maps) , in which case these items will be
destroyed and their memory cleaned up automatically as well.
**IMPORTANT!** When you create a data structure, the index value to
identify it is an integer value starting at 0. This means that data
structures of different types can have the **same** index value, so if
in doubt you should be using the [ ds_exists() ](../ds_exists)
function before accessing them. Also note that indices are re-used, so a
destroyed data structure index value may be used by a newly created one
afterwards so we recommend always setting the variable that held the DS
index to -1 after destroying.

#### Syntax:

``` gml
ds_map_destroy(id);
```

|          |                                                                                                          |                               |
|----------|----------------------------------------------------------------------------------------------------------|-------------------------------|
| Argument | Type                                                                                                     | Description                   |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the map to destroy. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ds_map_destroy(inventory); inventory = -1;
```

The above code will destroy the DS map with the id indexed in the
variable "inventory".
