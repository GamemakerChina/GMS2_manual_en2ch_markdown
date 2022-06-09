# os_type

This **read-only** variable holds one of various constant GameMaker has
to tell you which operating system the game has been created for. Note
that this is *not* necessarily the same as the OS of the device running
it, since - for example - your game could be running on an Amazon Fire
OS, but will have been built for the Android platform (in which case
os_type will be os_android ). The following constants can be returned:

|                                                                                                |                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------|
|  [OS Type Constant](../../../../GameMaker_Language/GML_Reference/OS_And_Compiler/os_type)  |                                       |
| Constant                                                                                       | Description                           |
|  os_windows                                                                                    | Windows OS                            |
|  os_uwp                                                                                        | Windows 10 Universal Windows Platform |
|  os_operagx                                                                                    | Opera GX                              |
|  os_linux                                                                                      | Linux                                 |
|  os_macosx                                                                                     | macOS X                               |
|  os_ios                                                                                        | iOS (iPhone, iPad, iPod Touch)        |
|  os_tvos                                                                                       | Apple tvOS                            |
|  os_android                                                                                    | Android                               |
|  os_ps4                                                                                        | Sony PlayStation 4                    |
|  os_ps5                                                                                        | Sony PlayStation 5                    |
|  os_xboxone                                                                                    | Microsoft Xbox One                    |
|  os_xboxseriesxs                                                                               | Microsoft Xbox Series X/S             |
|  os_switch                                                                                     | Nintendo Switch                       |
|  os_unknown                                                                                    | Unknown OS                            |

#### Syntax:

``` gml
os_type;
```

#### Returns:

``` gml
 OS Type Constant
```

#### Example:

``` gml
switch (os_type)
{
    case os_windows: global.Config = 0; break;
    case os_android: global.Config = 1; break;
    case os_linux: global.Config = 2; break;
    case os_macosx: global.Config = 3; break;
    case os_ios: global.Config = 4; break;
    case os_winphone: global.Config = 5; break;
}
```

The above code checks the OS running the game and sets a global variable
accordingly.
