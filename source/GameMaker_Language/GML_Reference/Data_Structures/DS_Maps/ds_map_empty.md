# ds_map_empty

This function will simply return false if the specified (previously
created) DS map contains any key/value pairs, or true if it does not.

#### Syntax:

``` gml
ds_map_empty(id);
```

|          |                                                                                                          |                                        |
|----------|----------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                     | Description                            |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the data structure to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if ds_map_empty(inventory)
{
    weight = 0;
}
```

The above code checks to see if the DS map indexed in the variable
"inventory" has any key/value pairs and if it does not it sets the
variable "weight" to 0.
