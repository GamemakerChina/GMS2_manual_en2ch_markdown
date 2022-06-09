# script_exists

This function will return true or false depending on whether the script
or [script function](../../../GML_Overview/Script_Functions) with
the given index exists. Note, that this is *not* a string, but rather
the asset name which holds the unique index for each script (as it would
appear in the IDE) or the named script function, as defined within the
script asset (note that this will not work for [method
variables](../../../GML_Overview/Method_Variables) ). For more
information on scripts, see [The Script
Editor](../../../../The_Asset_Editors/Scripts) .

#### Syntax:

``` gml
script_exists(scr);
```

|          |                                                                |                                          |
|----------|----------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                           | Description                              |
| scr      |  [Script Asset](../../../../../The_Asset_Editors/Scripts)  | The script index that you want to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
script[0] = -1;
script[1] = AI_Left;
script[2] = AI_Right;
var script_num = choose(0, 1, 2);
if script_exists(script[script_num])
{
    script_execute(script[script_num]);
}
```

The above example adds two script functions and a value into an array,
then proceeds to get a random number and use that to choose a script
function to run, unless the -1 is chosen in which case nothing will
happen.
