#  array_insert 

With this function you can insert a value (or values) into an array at
any given position. The function requires you to provide a variable that
holds the array, the index (position) in the array to insert at, as well
as at least *one* value to insert, although you can optionally provide
further arguments and they will all be inserted into the array in
consecutive order from the given index. Note that if the given index is
outside of the length of the array, the values will be added at the
given index, and any empty slots in the array between its last value and
the inserted values will be set to a default value of 0.

#### Syntax:

``` gml
array_insert(variable, index, value, [value], [value], [etc...]);
```

|                                  |                                                                                   |                                                          |
|----------------------------------|-----------------------------------------------------------------------------------|----------------------------------------------------------|
| Argument                         | Type                                                                              | Description                                              |
| variable                         |  [Array](../../../../GameMaker_Language/GML_Overview/Arrays)                  | The variable that holds the array.                       |
| index                            |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)               | The index (position) in the array to insert the value(s) |
| value                            |  [Variable](../../../../GameMaker_Language/GML_Overview/Data_Types#variable)  | The value to insert                                      |
| \[value\], \[value\], \[etc...\] |  [Variable](../../../../GameMaker_Language/GML_Overview/Data_Types#variable)  |  OPTIONAL Further values to insert into the array        |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
array_insert(score_array, score_rank, current_score);
```

The above code will insert the current score into the score array, at
the index defined by the score_rank variable.
