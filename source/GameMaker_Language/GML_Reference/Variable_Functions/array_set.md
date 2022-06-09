# array_set

With this function you can set the value of an index in an array to a
value. The function requires you to provide a variable that holds the
array as well as the index to set and the value to set it to. This
function can also be used for multi-dimension arrays, as long as you
specify which dimension you want to set when you supply the array index,
following this pattern:

``` gml
// 1D array
array_set(my_array, 0, 100);
// 2D array
array_set(my_array[0], 0, 100);
// 3D array
array_set(my_array[0][0], 0, 100);
// etc...
```

#### Syntax:

``` gml
array_set(variable, index, value);
```

|          |                                                                                   |                                                      |
|----------|-----------------------------------------------------------------------------------|------------------------------------------------------|
| Argument | Type                                                                              | Description                                          |
| variable |  [Array](../../../../GameMaker_Language/GML_Overview/Arrays)                  | The variable that holds the array.                   |
| index    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)               | The index of the array element to set the value for. |
| value    |  [Variable](../../../../GameMaker_Language/GML_Overview/Data_Types#variable)  | The value to set.                                    |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
for (var i = 0; i &amp;lt; 10; ++i;)
{
    array_set(score_array, i, i*100));
}
```

The above code will set the first 10 items in the given array to a
value.
