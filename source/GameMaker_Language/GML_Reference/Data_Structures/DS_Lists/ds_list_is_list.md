# ds_list_is_list

With this function you can check to see if another DS list is stored at
the given position within a DS list. If the given position contains a DS
list ID, then the function will return true otherwise it will return
false . Note that this will only detect lists that were manually
marked using the [ds_list_mark_as_list()](ds_list_mark_as_list)
function.

#### Syntax:

``` gml
ds_list_is_list(id, pos);
```

|          |                                                                                                             |                                        |
|----------|-------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                        | Description                            |
| id       |  [DS List ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The id of the list to check.           |
| pos      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The position within the list to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
var size = ds_list_size(ships);
for (var i = 0; i &amp;lt; size; i++)
{
    if ds_list_is_list(ships, i)
    {
        ds_list_destroy(ships[| i]);
    }
}
ds_list_destroy(ships);
```

The above code loops through a DS list and checks to see if any of the
entries contain other list IDs. If they do, then these lists are
destroyed, and then the main list is destroyed after the loop is
finished.
