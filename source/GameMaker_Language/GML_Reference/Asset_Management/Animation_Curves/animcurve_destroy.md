# animcurve_destroy

This function can be used to destroy any animation curves that have been
previously created with the function [ animcurve_create()
](animcurve_create) . Calling this function will remove the
animation curve from memory and clean up any channels or points that it
contains as well (these never need to be cleaned up manually). Note that
you **cannot destroy any animation curves created in the asset browser**
, only those created at runtime.

#### Syntax:

``` gml
animcurve_destroy(curve_struct);
```

|              |                                                                                                                                 |                                             |
|--------------|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| Argument     | Type                                                                                                                            | Description                                 |
| curve_struct |  [Animation Curve Struct](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Animation_Curves/animcurve_get)  | The pointer to the curve struct to destroy. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
animcurve_destroy(my_curve);
```

The above code will destroy the (previously created) animation curve
struct indexed in the variable " my_curve ".
