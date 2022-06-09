# path_get_length

You can use this function to get the exact length of a path in pixels.
this is *not* an approximate length from point to point, but rather an
exact length along the shape of the path, even when the path is smooth
with a high curved precision.

#### Syntax:

``` gml
path_get_length(index);
```

|          |                                                            |                                   |
|----------|------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                       | Description                       |
| index    |  [Path Asset](../../../../../The_Asset_Editors/Paths)  | The index of the path to measure. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
path_len = path_get_length(pth_AI);
```

This will set "path_len" to the total length of the path indexed in
"pth_AI" in pixels.
