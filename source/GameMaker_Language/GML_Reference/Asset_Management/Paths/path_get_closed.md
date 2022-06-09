# path_get_closed

This function can be used to return whether the path is flagged as
closed (true) or open (false), ie whether the path loops or if it has a
definitive beginning and end.

#### Syntax:

``` gml
path_get_closed(index);
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
state = path_get_closed(pth_Patrol);
```

This will set "state" to either true or false depending on the closed
state of the path indexed in "pth_Patrol".
