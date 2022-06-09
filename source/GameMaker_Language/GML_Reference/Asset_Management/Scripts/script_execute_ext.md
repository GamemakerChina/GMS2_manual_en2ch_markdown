# script_execute_ext

This function works similarly to the function
[script_execute()](script_execute) only you can supply an
[array](../../../GML_Overview/Arrays) that contains the arguments
required for the function/script being called. You may also supply two
optional arguments to the function to specify an offset into the array
to get the arguments from, as well as the number of arguments to use
from the array (this must be a maximum of array_length - offset).

#### Syntax:

``` gml
script_execute_ext(scr, array_args, [offset], [num_args]);
```

|              |                                                                                                                                                            |                                                                     |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| Argument     | Type                                                                                                                                                       | Description                                                         |
| scr          |  [Script Asset](../../../../../The_Asset_Editors/Scripts) or [Script Function](../../../../../GameMaker_Language/GML_Overview/Script_Functions)    | The function/script that you want to call                           |
| array_args   |  [Array](../../../../../GameMaker_Language/GML_Overview/Arrays)                                                                                        | The array containing the arguments for the function/script          |
| \[offset\]   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                     |  OPTIONAL The offset into the argument array                        |
| \[num_args\] |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                     |  OPTIONAL The number of arguments to use (from the offset onwards)  |

#### Returns:

``` gml
 Variable

(Will depend on the return value from the function/script being called)
```

#### Example:

``` gml
script_execute_ext(move_inst, move_array, floor(random(4)), 1);
```

The above example code will use script_execute_ext to call the given
function, supplying an array of four arguments, but only using one of
them at random. NOTE This function cannot be used with built-in
functions.
