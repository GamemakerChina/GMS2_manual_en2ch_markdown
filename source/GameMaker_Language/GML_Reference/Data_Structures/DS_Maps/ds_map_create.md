# ds_map_create

This function is used to create a new, empty, DS map and will return its
id which is then used to access the data structure in all other DS
map functions. **IMPORTANT!** When you create a data structure, the
index value to identify it is an integer value starting at 0. This means
that data structures of different types can have the **same** index
value, so if in doubt you should be using the [ ds_exists()
](../ds_exists) function before accessing them. Also note that
indices are re-used, so a destroyed data structure index value may be
used by a newly created one afterwards.

#### Syntax:

``` gml
ds_map_create();
```

#### Returns:

``` gml
 DS Map ID
```

#### Example:

``` gml
inventory = ds_map_create();
```

The above code will create a new, empty DS map and store its id index in
the variable "inventory".
