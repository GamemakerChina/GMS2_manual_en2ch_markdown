# weak_ref_any_alive

With this function you can check the weak reference to various structs
to see if it they are still "alive" or not. You supply an array of weak
references to check (each weak reference should have been created using
the function [ weak_ref_create() ](weak_ref_create) ), and the
function will return true if ***any*** of the structs are still being
referenced somewhere or false if they are not and have been garbage
collected. Note that if you supply an array where any of the values are
not a weak references, the function will return undefined . Note that
the function also takes two optional arguments, where the first permits
you to supply an initial index into the array to check from, as well as
an argument to set the number of positions (length) from that index to
check. If specified, only the array indices within those parameters will
be checked.

#### Syntax:

``` gml
weak_ref_any_alive(array, [index], [length]);
```

|            |                                                                                                                                                                                       |                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Argument   | Type                                                                                                                                                                                  | Description                                                                     |
| array      |  [Array](../../../../GameMaker_Language/GML_Overview/Arrays) of [Struct Weak Reference](../../../../GameMaker_Language/GML_Reference/Garbage_Collection/weak_ref_create) s    | Array containing weak references to the structs that you want to check.         |
| \[index\]  |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                   |  OPTIONAL The index into the array to start checking from                       |
| \[length\] |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                   |  OPTIONAL The number of positions, starting from the given index, to check for  |

#### Returns:

``` gml
 Boolean

(or undefined)
```

#### Example:

``` gml
if weak_ref_any_alive(inventory_ref_array)
{
    instance_destroy(obj_Inventory_Control);
}
```

The above code checks an array of weak references and if any are still
alive then an instance is destroyed.
