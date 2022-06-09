# path_get_name

This function will return the name of the path that is referenced as a
string. The name is whatever has been used to define the path in the
editor or (if the path has been created through a code function) it will
return a string with the format " \_newpathXX " where " XX " is the
number of the path generated, starting at 0 and incrementing by one
every time a new path is created. Please note that this is *only* a
string and cannot be used to reference the path directly - for that you
would need the *path index ID* . You can, however, use this string to
get the *path index ID* using the returned string along with the
function [ asset_get_index() ](../Assets_And_Tags/asset_get_index) .

#### Syntax:

``` gml
path_get_name(index);
```

|          |                                                            |                                 |
|----------|------------------------------------------------------------|---------------------------------|
| Argument | Type                                                       | Description                     |
| index    |  [Path Asset](../../../../../The_Asset_Editors/Paths)  | The index of the path to check. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
path_name = path_get_name(path_array[0]);
```

This will set "path_name" to the name of the path indexed in the given
array at position 0.
