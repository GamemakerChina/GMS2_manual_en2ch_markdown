# path_get_number

This function can be used to return the number of points on a path.

#### Syntax:

``` gml
path_get_number(index);
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
if (path_get_number(pth_AI) &amp;gt; 1)
{
    path_start( pth_AI, 4, 3, 0);
}
```

The above code checks to see if a path has more than one point on it and
if so it starts the instance moving along that path.
