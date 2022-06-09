# array_push

With this function you can push a value (or values) onto the end of an
array without having to know the length of the array. The function
requires you to provide a variable that holds the array as well as at
least *one* value to push, although you can optionally provide further
arguments and they will all be pushed onto the array in consecutive
order.

#### Syntax:

``` gml
array_push(variable, value, [value], [value], [etc...]);
```

|                                  |                                                                                   |                                                       |
|----------------------------------|-----------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument                         | Type                                                                              | Description                                           |
| variable                         |  [Array](../../../../GameMaker_Language/GML_Overview/Arrays)                  | The variable that holds the array.                    |
| value                            |  [Variable](../../../../GameMaker_Language/GML_Overview/Data_Types#variable)  | The value to push onto the end of the array           |
| \[value\], \[value\], \[etc...\] |  [Variable](../../../../GameMaker_Language/GML_Overview/Data_Types#variable)  |  OPTIONAL Further values to be pushed onto the array  |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
array_push(score_array, obj_Player1.scr, obj_Player2.scr, obj_Player3.scr, obj_Player4.scr);
```

The above code will push four values onto the end of the given array.
