# os_browser

This **read-only** variable holds one of various constants (listed
below) that GameMaker has to tell you which browser you are currently
running the game in (if any).

#### Syntax:

``` gml
os_browser
```

#### Returns:

``` gml
 Browser Type Constant
```

|                                                                                                        |                                       |
|--------------------------------------------------------------------------------------------------------|---------------------------------------|
|  [Browser Type Constant](../../../../GameMaker_Language/GML_Reference/OS_And_Compiler/os_browser)  |                                       |
| Constant                                                                                               | Description                           |
|  browser_not_a\_browser                                                                                | Game is not being played in a browser |
|  browser_unknown                                                                                       | Unknown browser                       |
|  browser_ie                                                                                            | Internet Explorer                     |
|  browser_ie_mobile                                                                                     | Internet Explorer on a mobile device  |
|  browser_firefox                                                                                       | Mozilla Firefox                       |
|  browser_chrome                                                                                        | Google Chrome                         |
|  browser_safari                                                                                        | Safari                                |
|  browser_safari_mobile                                                                                 | Safari on a mobile device             |
|  browser_opera                                                                                         | Opera                                 |
|  browser_tizen                                                                                         | Tizen mobile device browser           |
|  browser_windows_store                                                                                 | Windows App                           |

#### Example:

``` gml
if (os_browser == browser_not_a_browser)
{
    global.Config = 0;
}
else
{
    global.Config = 1;
}
```

The above code checks to see if the game is running in a browser or not
and sets a global variable to a value depending on the result of the
check.
