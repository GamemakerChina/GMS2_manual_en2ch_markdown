# array_length_1d  DEPRECATED 

**WARNING!** This function is deprecated (and replaced by
[array_length()](array_length) ) as arrays are no longer limited to
only 1 or 2 dimensions, and as such this function is only supplied for
support of legacy projects. All new projects should use the current way
of creating and accessing multi-dimension arrays (see
[here](../../GML_Overview/Arrays) for more information). With this
function you can get the length (number of entries) of a 1D array. For
2D arrays you should be using the [ array_height_2d
](array_height_2d) and [ array_length_2d ](array_length_2d)
functions. **IMPORTANT!:** If the array has over 32,000 entries this
function will return an erroneous value and should not be used.

#### Syntax:

``` gml
array_length_1d(array_index);
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
for (var i = array_length_1d(a) - 1; i &amp;gt; -1; i--;)
{
    a[i] = -1;
}
```

The above code will loop through an array and set each entry to -1.
