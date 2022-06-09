# show_debug_message

This function will create a custom debug message that is shown in the
compiler window at runtime. Note that the message can be *either* a
string or a real number, but if you need both then the number will have
to be converted to string first using the [ string()
](../Strings/Strings) function (see the example below) and that if
the number has more than two decimal places then you should use [
string_format() ](../Strings/string_format) to show them as by
default decimals are rounded to the nearest two decimal places (so
"1.2468" would show as "1.25" in the output window). Debug messages
shown with this function will be shown in the [Compiler Output
Window](../../../Introduction/The_Output_Window) at the bottom of
the IDE as well as in the [Graph
View](../../../IDE_Tools/The_Debugger) of the debugger when running
the game in Debug Mode. If you only want to see messages in Debug Mode
then you should probably be using [ debug_event() ](debug_event)
instead.

#### Syntax:

``` gml
show_debug_message(string);
```

|          |                                                                        |                                   |
|----------|------------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                                   | Description                       |
| string   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The custom debug message to show. |

#### Returns:

``` gml
N/A
```

#### **Example:**

``` gml
if !instance_exists(obj_Exit)
{
    show_debug_message("Exit not created!");
    show_debug_message("Error Num: " + string(global.error));
    game_end();
}
```

The above code checks to see if an instance exists and if it does not, a
debug message is shown in the compile window and the game is ended.
