# array_equals

With this function you can check to see if two arrays are equal
(equivalent or the same). You give the two arrays to check, and the
function will return true if they are equal (either equivalent or the
same) or false if they are not. Note that this is *not* the same as
checking if two arrays are the same using ==, which will not check to
see if the two arrays hold equivalent values, but only to see if the
arrays are referencing the same initial array. For example:

``` gml
var a = [1,2,3,4];
var b = [1,2,3,4];

if (a == b)
{
    show_debug_message( "This will never fire, as a and b do not reference the SAME array" );
}

if (array_equals(a, b))
{
    show_debug_message( "This will fire as both arrays contain similar values" );
}
```

Note that there are some constants that may not be equal to themselves,
which can make this function fail. Here is an example:

``` gml
if (array_equals([NaN], [NaN]))
{
    show_debug_message( "This will never fire as NaN cannot be equal to itself" );
}
```

See the [Equality
Table](../../../Additional_Information/Type_Tables#h) for more
information.

#### Syntax:

``` gml
array_equals(var1, var2);
```

|          |                                                                   |                   |
|----------|-------------------------------------------------------------------|-------------------|
| Argument | Type                                                              | Description       |
| var1     |  [Array](../../../../GameMaker_Language/GML_Overview/Arrays)  | The first array.  |
| var2     |  [Array](../../../../GameMaker_Language/GML_Overview/Arrays)  | The second array. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !array_equals(inventory_array, item_array)
{
    var len = array_length(inventory_array);
    array_copy(item_array, 0, inventory_array, 0, len);
}
```

The above code will check two arrays to see if they hold equivalent
values, and if they do not then the code will copy the entire contents
of the array "inventory_array" to the array "item_array".
