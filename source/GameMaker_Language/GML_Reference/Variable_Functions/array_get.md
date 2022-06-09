# array_get

With this function you can retrieve the value from an index in an array.
The function requires you to provide a variable that holds the array and
the index to get the value from within that array. Note that if the
array index given is out of bounds then the game will crash with an
error. This function can also be used for multi-dimension arrays, as
long as you specify which dimension you want to get when you supply the
array index, following this pattern:

``` gml
// 1D array
array_get(my_array, 0);
// 2D array
array_get(my_array[0], 0);
// 3D array
array_get(my_array[0][0], 0);
// etc...
```

#### Syntax:

``` gml
array_get(variable, index);
```

|          |                                                                      |                                                       |
|----------|----------------------------------------------------------------------|-------------------------------------------------------|
| Argument | Type                                                                 | Description                                           |
| variable |  [Array](../../../../GameMaker_Language/GML_Overview/Arrays)     | The variable that holds the array.                    |
| index    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The index of the array element to get the value from. |

#### Returns:

``` gml
 Variable

(Any valid data type that an array can hold)
```

#### Example:

``` gml
for (var i = 0; i &amp;lt; 10; ++i;)
{
    show_debug_message(array_get(my_array, i));
}
```

The above code will output the first 10 items of the given to the
console.
