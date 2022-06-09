# array_create

With this function you can create a 1D array of a given size. You tell
the function the length of the array to create, and it will return the
"handle" for the array which you can then assign to a variable. Arrays
created in this way will have each entry initialised to 0 unless you
specify an (optional) initialisation value. If you do supply the extra
value for initialising the array, then all indices within the new array
will be set to that instead of 0, but note that the function will have a
greater performance overhead in this case.

#### Syntax:

``` gml
array_create(size, [value]);
```

|          |                                                                                   |                                                              |
|----------|-----------------------------------------------------------------------------------|--------------------------------------------------------------|
| Argument | Type                                                                              | Description                                                  |
| size     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)               | The size of the array to create.                             |
| value    |  [Variable](../../../../GameMaker_Language/GML_Overview/Data_Types#variable)  |  OPTIONAL The value to use to initialise all array indices.  |

#### Returns:

``` gml
 Array
```

#### Example:

``` gml
instance_array = array_create(100, noone);
```

The above code will create a new array of 100 entries, each one set to
the keyword noone , and then assign it to the variable "instance_array".
