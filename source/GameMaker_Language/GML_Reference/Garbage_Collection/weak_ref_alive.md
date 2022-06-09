# weak_ref_alive

With this function you can check the weak reference to a struct to see
if it is still "alive" or not. You supply the weak reference to check
(as returned by the function [ weak_ref_create() ](weak_ref_create)
), and the function will return true if the struct is still being
referenced somewhere or false if it's not and has been garbage
collected. Note that if you supply a value that is not a weak reference,
the function will return undefined .

#### Syntax:

``` gml
weak_ref_alive(weak_ref);
```

|          |                                                                                                                |                                                     |
|----------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument | Type                                                                                                           | Description                                         |
| weak_ref |  [Struct Weak Reference](../../../../GameMaker_Language/GML_Reference/Garbage_Collection/weak_ref_create)  | The weak reference to the struct you want to check. |

#### Returns:

``` gml
 Boolean

(or undefined)
```

#### Example:

``` gml
if weak_ref_alive(inventory_ref)
{
    inventory = -1;
}
```

The above code checks a weak reference to a struct and if it is still
alive the variable referencing it is set to -1, de-referencing the
struct and enabling it to be garbage collected.
