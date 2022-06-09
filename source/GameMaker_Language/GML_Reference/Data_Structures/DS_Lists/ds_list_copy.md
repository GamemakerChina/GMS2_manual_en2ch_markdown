# ds_list_copy

With this function you can copy the contents of one list into another.
Both lists must have been created previously and if the list being
copied *to* already has information within it, this list will be cleared
first. The end result is two independent lists which contain the same
information.

#### Syntax:

``` gml
ds_list_copy( id, source );
```

|          |                                                                                                             |                                          |
|----------|-------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                                                                        | Description                              |
| id       |  [DS List ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The id of the list being copied *to* .   |
| source   |  [DS List ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The id of the list to be copied *from* . |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if !ds_list_empty(main_list)
{
    old_list = ds_list_create();
    ds_list_copy(old_list, main_list);
    ds_list_clear(main_list);
}
```

The above code will check a DS list to see if it is empty. If it is not
empty it is copied into another DS list (which has been created
previously) and then the original list is cleared.
