# OS And Compiler

When creating cross-platform games, it is often of vital importance that
you get the details of the operating system that the device running your
game is using. Things like the language, the version or the network
state can all be used to adapt your game to the system running it and
make the end-user experience the best possible, so GameMaker has a
number of special functions which can be used to get the necessary
information. The following functions and variables exist for you to use
to get certain details about the operating system or browser that is
running your game:

-   [os_browser](os_browser)
-   [os_device](os_device)
-   [os_type](os_type)
-   [os_version](os_version)
-   [os_is_paused](os_is_paused)
-   [os_is_network_connected](os_is_network_connected)
-   [os_get_config](os_get_config)
-   [os_get_language](os_get_language)
-   [os_get_region](os_get_region)
-   [os_get_info](os_get_info)
-   [os_powersave_enable](os_powersave_enable)
-   [os_lock_orientation](os_lock_orientation)
-   [os_check_permission](os_check_permission)
-   [os_request_permission](os_request_permission)

Certain functions are *pre-compiled* when you run your game (ie: they
are used to define how the final game will be compiled), and some are
also for use when the game has been compiled to get specific details
about the runtime environment. Here you can find the full list of these
functions:

-   [GM_build_date](GM_build_date)
-   [GM_version](GM_version)
-   [GM_runtime_version](GM_runtime_version)
-   [gml_release_mode](gml_release_mode)
-   [gml_pragma](gml_pragma)
-   [parameter_count](parameter_count)
-   [parameter_string](parameter_string)
-   [environment_get_variable](environment_get_variable)

On Windows, the resolution of the Windows thread scheduler is set to 1ms
by default when your game runs. The following functions are available
for retrieving and changing the resolution of the Windows thread
scheduler at runtime:

-   [scheduler_resolution_get](scheduler_resolution_get)
-   [scheduler_resolution_set](scheduler_resolution_set)

Finally, when working with
[Extensions](../../../The_Asset_Editors/Extensions) you may need to
be able to define and call external functions at runtime, and so you'd
use the following: **NOTE** : These are legacy functions and you should
define any extension functions within the Extension Editor itself.
**NOTE** : These functions are for the **Windows** and **macOS** target
platforms only.

-   [external_define](external_define)
-   [external_call](external_call)
-   [external_free](external_free)
