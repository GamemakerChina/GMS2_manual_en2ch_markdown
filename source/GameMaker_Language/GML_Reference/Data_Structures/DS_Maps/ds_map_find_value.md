# ds_map_find_value

With this function you can get the value from a specified key. The input
values of the function are the (previously created) DS map to use and
the key to check for. **NOTE** : If no such key exists then the function
will return undefined . You should always check this using the [
is_undefined() ](../../Variable_Functions/is_undefined) function

#### Syntax:

``` gml
ds_map_find_value(id, key)
```

|          |                                                                                                          |                           |
|----------|----------------------------------------------------------------------------------------------------------|---------------------------|
| Argument | Type                                                                                                     | Description               |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the map to use. |
| key      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                 | The key to find.          |

#### Returns:

``` gml
 Variable

or

 undefined
```

#### Example:

``` gml
amount = ds_map_find_value(inventory, "food");
```

Or, using the map [accessor](../../../GML_Overview/Accessors) "?":

``` gml
amount = inventory[? "food"];
```

The above code will get the value of the key "food" and store it in the
variable "amount".
