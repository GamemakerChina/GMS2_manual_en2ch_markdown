# debug_get_callstack

This function generates an array of strings as the "callstack" where the
current script is listed first, and then all the other scripts that were
run in order for the current script to be executed. The exact string
format will vary depending on the target platform chosen, but it will
mostly have the script/event name, then a colon : and the line number,
similar to this:

``` gml
"gml_Script_script2:1"
  "gml_Script_script1:32"
  "gml_Script_script0:64"
  "gml_Object_object0_Create_0:1"
```

The function allows for an optional argument to be passed in, which
is the maximum depth of the returned callstack. This value is the number
of scripts that are included in the returned array starting from the
current script. If this argument is not specified, then the full
callstack will be returned. Note that the returned array will always
contain 0 in its last position, after listing the callstack scripts.

#### Syntax:

``` gml
debug_get_callstack([maxdepth])
```

|              |                                                                      |                                                                |
|--------------|----------------------------------------------------------------------|----------------------------------------------------------------|
| Argument     | Type                                                                 | Description                                                    |
| \[maxdepth\] |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  |  OPTIONAL The maximum depth of the callstack that is returned  |

#### Returns:

``` gml
 Array
```

#### **Example:**

``` gml
if debug_mode
{
    if keyboard_check(vk_escape)
    {
        var _a = debug_get_callstack(4);
        for (var i = 0; i &amp;lt; array_length_id(_a); ++i;)
        {
            show_debug_message(_a[i]);
        }
    }
}
```

The above code checks to see if debug mode is enabled and if it is,
checks to see if a key is being held down. In that case, it outputs the
current call stack to the console, with a maximum depth of 4.
