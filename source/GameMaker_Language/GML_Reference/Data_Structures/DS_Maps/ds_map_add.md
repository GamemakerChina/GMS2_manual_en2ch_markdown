# ds_map_add

This function should be used to add sets of key/value pairs into the
specified DS map . You can check this function to see if it was
successful or not (it will return true on success or false otherwise),
as it may fail if there already exists the same key in the DS map or you
specify a non-existent DS map as the ID of the map to add to. The keys
and and values you supply can be made up of any combination of data
types, so all of the following - and more - are acceptable (although, in
practice, you would most commonly use a string for the key):

``` gml
ds_map_add(map, 5, undefined); ds_map_add(map, "level", 1); ds_map_add(map, 89.6, "hello world"); ds_map_add(map, 5, buffer_get_address(buff));
```

You can also add to a map using the
[accessor](../../../GML_Overview/Accessors) " ? ", as shown below:

``` gml
map[? 5] = undefined; map[? "level"] = 1; map[? 89.6] = "hello world"; map[? 5] = buffer_get_address(buff);
```

**NOTE** : Unlike other data structures in GameMaker this key will not
go to the start (nor the end) of the DS map , but rather it will just go
into the DS map **somewhere** .

#### Syntax:

``` gml
ds_map_add(id, key, val);
```

|          |                                                                                                          |                              |
|----------|----------------------------------------------------------------------------------------------------------|------------------------------|
| Argument | Type                                                                                                     | Description                  |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the map to add to. |
| key      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                 | The key of the value to add. |
| val      |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                      | The value to add to the map. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
inventory = ds_map_create(); ds_map_add(inventory, "hp potion", 1); ds_map_add(inventory, "gold", 100);
```

This will create a new map, assigning its id to the variable
"inventory". It then adds two new keys to the map, "hp potion" and
"gold", and sets their initial values as 1 and 100.
