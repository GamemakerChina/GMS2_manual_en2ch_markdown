#  array_delete 

With this function you can delete a value (or values) from an array at
any given position. The function requires you to provide a variable that
holds the array, the index (position) in the array to delete from, as
well as the number of values to delete.

#### Syntax:

``` gml
array_delete(variable, index, number);
```

|          |                                                                      |                                                                |
|----------|----------------------------------------------------------------------|----------------------------------------------------------------|
| Argument | Type                                                                 | Description                                                    |
| variable |  [Array](../../../../GameMaker_Language/GML_Overview/Arrays)     | The variable that holds the array.                             |
| index    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The index (position) in the array to delete the value(s) from. |
| number   |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The number of values to delete.                                |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
array_delete(score_array, 0, 10);
```

The above code will delete the first 10 values in the given array
starting at index 0 (so indices 0 to 9 will be removed from the array).
