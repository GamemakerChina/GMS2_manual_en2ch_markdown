# path_duplicate

This function takes a path and copies it into a new path. The new path
is created in the process, and its index is returned to be used in all
further calls to use this new path.

#### Syntax:

``` gml
path_duplicate(index);
```

|          |                                                               |                                              |
|----------|---------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                          | Description                                  |
| index    |  [Path Asset](../../../../../../The_Asset_Editors/Paths)  | The index of the existing path to duplicate. |

#### Returns:

``` gml
 Path Asset
```

#### Example:

``` gml
mypath = path_duplicate(choose(pth_1, pth_2, pth_3, pth_4));
```

The above code chooses one of four path resources and duplicates it,
storing the index of the new path in the variable "mypath".
