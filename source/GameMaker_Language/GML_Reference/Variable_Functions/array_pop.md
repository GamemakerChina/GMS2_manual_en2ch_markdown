# array_pop

This function will remove the last element in the given array, and
return its value. If the array is empty, undefined is returned.

#### Syntax:

``` gml
array_pop(array);
```

|          |                                                                   |                                          |
|----------|-------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                              | Description                              |
| array    |  [Array](../../../../GameMaker_Language/GML_Overview/Arrays)  | The array to remove the last value from. |

#### Returns:

``` gml
 Variable

or

 undefined
```

#### Example:

``` gml
var _lastscore = array_pop(score_array);
draw_text(32, 32, "Last Score = " + string(_lastscore));
```

The above code will pop the last value from the given array, and then
draw it along with some text to the screen. The retrieved entry is also
removed from the score array.
