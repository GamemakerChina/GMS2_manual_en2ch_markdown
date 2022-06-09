# ds_map_replace

With this function you can change the value for the given key within the
a DS map . You supply the index to the map (as returned by the function
[ ds_map_create() ](ds_map_create) ) and then the key to replace -
either a string or an integer - and the value to replace the key value
with. If the given key does *not* exist then it will be created for you,
and if it does then the current value will be replaced with the new
value. The function will return true if the key exists and the value is
replaced, and false if the key does not exist and a new key was created
with the value.

#### Syntax:

``` gml
ds_map_replace( id, key, val );
```

|          |                                                                                                          |                                                               |
|----------|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Argument | Type                                                                                                     | Description                                                   |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the map to change.                                  |
| key      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                 | The key with the value that should be replaced by the new one |
| val      |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                      | The new value to replace the given value with                 |

#### Returns:

``` gml
 Boolean
```

#### **Example:**

``` gml
ds_map_replace(inventory, "torso", 55);
```

The above code looks up the DS map for the key "torso" and when it finds
it (or it is created if it doesn't exist) the current value is replaced
with the one specified.
