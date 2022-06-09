# ds_list_find_value

With this function you can check the given list position and the value
held within the list for that position will be returned. Note that if
you give a position that is outside of the given list size (i.e.:
position 11 in a 10 value list) then the function may return undefined
*or* 0. This is because when you create the list, internally the first
few entries in the list are set to 0 to minimize performance issues when
initially adding items to the list (although the [ ds_list_size()
](ds_list_size) function will still return 0 on a newly created
list). If you wish to ensure that the list is "truly" empty on create,
then you should call [ ds_list_clear() ](ds_list_clear) after
creating the list, which will then mean that any values returned for
unpopulated list slots will be undefined , which you can then check
consistently using the [ is_undefined()
](../../Variable_Functions/is_undefined) function.

#### Syntax:

``` gml
ds_list_find_value(id, pos);
```

|          |                                                                                                             |                                                                                                                                 |
|----------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                        | Description                                                                                                                     |
| id       |  [DS List ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The id of the list to use.                                                                                                      |
| pos      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The position to look at, where 0 corresponds to the very beginning of the list and the final position is ds_list_size(id)-1 .   |

#### Returns:

``` gml
 Variable

or

 undefined
```

#### Example:

``` gml
val = ds_list_find_value(list, ds_list_size(list) - 1);
```

The above code checks the list indexed in the variable "list" at the
last position in the list and stores the returned value in the variable
"val".
