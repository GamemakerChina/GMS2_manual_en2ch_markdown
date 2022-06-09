# path_get_precision

This function returns with what precision the given path has been
"smoothed", and will be an integer value from 1 to 8. Although you can
get (and set) this value for a straight-line path it will have no
influence over how an instance uses the path as it is only relevant when
the path kind is set to "smooth".

#### Syntax:

``` gml
path_get_precision(index);
```

|          |                                                            |                                 |
|----------|------------------------------------------------------------|---------------------------------|
| Argument | Type                                                       | Description                     |
| index    |  [Path Asset](../../../../../The_Asset_Editors/Paths)  | The index of the path to check. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if (path_get_kind(pth_Patrol))
{
    if (path_get_precision(pth_Patrol)) != 8
    {
        path_set_precision(pth_Patrol, 8);
    }
}
```

The above code checks the path indexed in "pth_Patrol" to see what kind
it is and if it is smooth, it then checks how precise the smoothing is.
If it is less than 8, it is then set to a value of 8.
