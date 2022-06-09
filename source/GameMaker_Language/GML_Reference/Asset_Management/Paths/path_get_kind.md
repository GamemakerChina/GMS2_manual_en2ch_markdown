# path_get_kind

Paths can be either *smooth* or *straight* (a smooth path calculates a
curved path around the defining points, whereas a straight path just
goes straight from one point to another). This function can be used to
find out whether the given path is smooth ( true ) or not ( false ).

#### Syntax:

``` gml
path_get_kind(index);
```

|          |                                                            |                                 |
|----------|------------------------------------------------------------|---------------------------------|
| Argument | Type                                                       | Description                     |
| index    |  [Path Asset](../../../../../The_Asset_Editors/Paths)  | The index of the path to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
path_kind = path_get_kind(pth_Patrol);
```

This will set the "path_kind" variable to true or false depending on the
kind of path the given path index is.
