# array_length

With this function you can get the length (number of entries) of an
array dimension. You supply the array index value and the function will
return an integer value representing the number of entries the array
contains. This function can also be used for multi-dimension arrays, as
long as you specify which dimension you want to get the length of when
you supply the array index, following this pattern:

``` gml
// Returns the first dimension of the array
val = array_length(my_array);

// Returns the second dimension of the array
val = array_length(my_array[0]);

// Returns the third dimension of the array
val = array_length(my_array[0][0]);

// etc...
```

#### Syntax:

``` gml
array_length(array_index);
```

|             |                                                                   |                                  |
|-------------|-------------------------------------------------------------------|----------------------------------|
| Argument    | Type                                                              | Description                      |
| array_index |  [Array](../../../../GameMaker_Language/GML_Overview/Arrays)  | The index of the array to check. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
for (var i = 0; i &amp;lt; array_length(a); ++i)
{
    a[i] = -1;
}
```

The above code will loop through an array and set each entry to -1.
