# object_index

This **read only** variable returns the index of the object that the
instance has been created from. This is *not* the same as the object
name, which is a string and can be found using [ object_get_name()
](object_get_name) , as this function returns the index number,
which is a unique value that GameMaker assigns to every object at the
time of creation.

#### Syntax:

``` gml
object_index;
```

#### Returns:

``` gml
 Object Asset
```

#### Example:

``` gml
obj_name = object_get_name(object_index);
```

The above code will use the object_index to find the name of the object
that the current instance has been created from.
