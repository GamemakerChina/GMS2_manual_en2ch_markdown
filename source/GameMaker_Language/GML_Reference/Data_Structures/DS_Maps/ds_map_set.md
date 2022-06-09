# ds_map_set

With this function you can set the value of a key within a given DS map.
You supply the DS map ID value (as returned by the function [
ds_map_create() ](ds_map_create) ), then give the key you want to
set and the value to set it to. Keys can be integers or strings, and if
the given key does not exist then it will be created for you and set to
the value. This function is the same as using the [DS map
accessor](../../../GML_Overview/Accessors) to set/create a map
key/value pair. The function does not return anything, so if you need to
check if the key value has been replaced or a new key has been created,
then you should use the function [ds_map_replace()](ds_map_replace)
.

#### Syntax:

``` gml
ds_map_set(id, key, value)
```

|          |                                                                                                          |                              |
|----------|----------------------------------------------------------------------------------------------------------|------------------------------|
| Argument | Type                                                                                                     | Description                  |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the map to use.    |
| key      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                 | The key to set.              |
| value    |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                      | The value to set the key to. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if is_undefined(ds_map_find_value(map, "score"))
{
    ds_map_set(map, "score", 0);
}
```

The above code will check to see if the given key exists and if it
doesn't then it is created and set.
