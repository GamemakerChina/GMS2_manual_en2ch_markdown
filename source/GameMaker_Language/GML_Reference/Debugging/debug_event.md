# debug_event

This function generates a custom debug event that will be shown in the
Graph View of the debugger when a game is being run in [Debug
Mode](../../../Introduction/Debugging) . If you require messages to
be displayed when *not* in debug mode, use [ show_debug_message()
](show_debug_message) . The function will also take two reserved
strings to help perform debugging using external applications like
Visual Studio. These strings are:

-   " OutputDebugOn " - This enables a call to OutputDebugString for the
    **Windows** target, which means that all debug output - everything
    you see in the Output window - can be viewed by Visual Studio or by
    3rd party apps.
-   " OutputDebugOff " - Disables the behaviour described above.
-   " BreakOnError " - This option is for **Windows YYC** builds only,
    and means that projects will *not* display the usual code error
    screen if the runtime detects an error, but instead just carry on
    and crash. This allows you to see the stacktrace within Visual
    Studio if debugging.
-   " ResourceCounts " - Lists all the currently active resources, such
    as Data Structures, Time Sources, Surfaces, etc.
-   " DumpMemory " - Gives information on the current memory usage.

#### Syntax:

``` gml
debug_event(string)
```

|          |                                                                        |                                       |
|----------|------------------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                                   | Description                           |
| string   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The custom debug event string to use. |

#### Returns:

``` gml
N/A
```

#### **Example:**

``` gml
if !surface_exists(global.EffectsSurface)
{
    debug_event("Recreating Effects Surface");
    global.EffectsSurface = surface_create(room_width, room_height);
}
```

The above code checks to see if an surface exists and if it does not, a
debug event is triggered in the graph view of the debugger (the game
must have been run in Debug Mode for this to be visible) and the surface
is recreated.
