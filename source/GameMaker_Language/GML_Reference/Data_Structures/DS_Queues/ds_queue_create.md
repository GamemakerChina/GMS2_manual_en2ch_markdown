# ds_queue_create

This function will create a new queue data-structure and return the
index value. This value should be stored in a variable and used in all
further function calls relating to the queue. **IMPORTANT!** When you
create a data structure, the index value to identify it is an integer
value starting at 0. This means that data structures of different types
can have the **same** index value, so if in doubt you should be using
the [ ds_exists() ](../ds_exists) function before accessing them.
Also note that indices are re-used, so a destroyed data structure index
value may be used by a newly created one afterwards.

#### Syntax:

``` gml
ds_queue_create();
```

#### Returns:

``` gml
 DS Queue ID
```

#### Example:

``` gml
queue = ds_queue_create();
```

This will create a new queue and assign its index id to the instance
variable "queue".
