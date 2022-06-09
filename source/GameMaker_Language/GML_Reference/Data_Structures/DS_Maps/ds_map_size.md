# ds_map_size

With this function you can find how many key/values pairs the
(previously created) DS map contains.

#### Syntax:

``` gml
ds_map_size(id);
```

|          |                                                                                                          |                                        |
|----------|----------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                     | Description                            |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the data structure to check. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if (ds_map_size(inventory) &amp;gt; 49)
{
    full = true;
}
```

The above code will check the size of the DS map (ie: number of
key/value pairs) and if it is greater than 49 it sets the variable
"full" to true .
