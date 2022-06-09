# ds_list_delete

With this function you can remove the value stored at a specific
position within the list.

#### Syntax:

``` gml
ds_list_delete(id, pos);
```

|          |                                                                                                             |                                        |
|----------|-------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                        | Description                            |
| id       |  [DS List ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The id of the list to change.          |
| pos      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | Where in the list to delete the value. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (ds_list_size(sc_list) &amp;gt; 10)
{
    while (ds_list_size(sc_list) &amp;gt; 10)
    {
        ds_list_delete(sc_list, 0);
    }
}
```

The above code checks the size of a DS list and if it is larger than
ten, it loops through the list removing the top value (position 0) until
the list has only 10 entries.
