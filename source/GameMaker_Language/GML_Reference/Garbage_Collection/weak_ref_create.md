# weak_ref_create

With this function you can create a weak reference to a struct which can
then be used to check if the struct is still "alive" (referenced) or not
in the game. You supply the reference to the struct you want to track,
and the function will return another struct which is a weak reference to
that struct. Note that you can check whether a reference is "strong" or
"weak" by using the function
[instanceof()](../Variable_Functions/instanceof) , as a strong
reference will return either " struct " or the name of the constructor
function that created the struct, or " weakref " if it's a weak
reference. Also note that the weak reference struct will have a variable
" ref " which can be accessed to get the strong reference to the struct
in question, unless it has been garbage collected, in which case it will
return undefined .

#### Syntax:

``` gml
weak_ref_create(struct_to_track);
```

|                 |                                                                     |                                                         |
|-----------------|---------------------------------------------------------------------|---------------------------------------------------------|
| Argument        | Type                                                                | Description                                             |
| struct_to_track |  [Struct](../../../../GameMaker_Language/GML_Overview/Structs)  | The struct that you want to create a weak reference for |

#### Returns:

``` gml
 Struct Weak Reference
```

#### Example:

``` gml
inventory_ref = weak_ref_create(inventory);
```

The above code creates a weak reference to a struct and stores it in an
instance variable for later use.
