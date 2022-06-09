# method_get_index

With this function you can retrieve the
[Script](../../GML_Overview/Script_Functions) index for the script
where the method was defined. If the method was not defined in a script
then the function will return -1, otherwise it will return the index
value for the script.

#### Syntax:

``` gml
method_get_index(method);
```

|          |                                                                              |                              |
|----------|------------------------------------------------------------------------------|------------------------------|
| Argument | Type                                                                         | Description                  |
| method   |  [Method](../../../../GameMaker_Language/GML_Overview/Method_Variables)  | The method variable to check |

#### Returns:

``` gml
 Script Asset

or

 Real
```

#### Example:

``` gml
var _index = method_get_index(light_setup);
if _index != -1
{
    show_debug_message(script_get_name(_index));
}
```

The above code will check the script index for the method "light_setup"
and then if it is not -1 it will output the script name to the console.
