# script_get_name

This function will return the name *as a string* of the specified
script. This name is the one that has been specified for the script in
the Asset Browser of the main GameMaker window. For more information
about scripts, see [The Script
Editor](../../../../The_Asset_Editors/Scripts) .

#### Syntax:

``` gml
script_get_name(scr);
```

|          |                                                                |                                                           |
|----------|----------------------------------------------------------------|-----------------------------------------------------------|
| Argument | Type                                                           | Description                                               |
| scr      |  [Script Asset](../../../../../The_Asset_Editors/Scripts)  | The index of the script that you want to get the name of. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
scr_name = script_get_name(Help_File);
```

The above example code will store the name of the indicated script index
in the variable "scr_name".
