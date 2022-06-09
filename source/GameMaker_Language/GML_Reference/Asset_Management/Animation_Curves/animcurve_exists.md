# animcurve_exists

This function will return true if the given [Animation Curve
Asset](../../../../../The_Asset_Editors/Animation_Curves) or
[Animation Curve
Struct](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Animation_Curves/animcurve_get)
exists and is a valid Animation Curve, or false if it isn't.

#### Syntax:

``` gml
animcurve_exists(curve_struct_or_id);
```

|                    |                                                                                                                                                                                                                     |                                           |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| Argument           | Type                                                                                                                                                                                                                | Description                               |
| curve_struct_or_id |  [Animation Curve Struct](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Animation_Curves/animcurve_get) or [Animation Curve Asset](../../../../../The_Asset_Editors/Animation_Curves)    | The Animation Curve that will be checked. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if (animcurve_exists(spring_curve))
{
    apply_spring_animation(sprite_curve);
}
```

The above code checks if the Animation Curve stored in the custom
spring_curve variable exists. If it does, it runs a custom method to use
that Animation Curve.
