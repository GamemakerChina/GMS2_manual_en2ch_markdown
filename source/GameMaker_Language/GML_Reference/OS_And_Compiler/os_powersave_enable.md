# os_powersave_enable

With this function you can turn on or off the power saving features of
the device. This is important as certain games (for example those that
use the tilt functions) may not generate events that the OS can
interpret as being user input and so shut down the screen or exit the
game. By setting this function to false you can disable the power saving
features and ensure that the screen (and game) are always functioning.
**NOTE** : This is limited to iOS and Android targets.

#### Syntax:

``` gml
os_powersave_enable(flag)
```

|          |                                                                         |                                                                    |
|----------|-------------------------------------------------------------------------|--------------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                        |
| flag     |  [Boolean](../../../../GameMaker_Language/GML_Overview/Data_Types)  | Set to true or false to enable or disable powersave functions.     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (os_type == os_android) || (os_type == os_ios)
{
    os_powersave_enable(false);
}
```

The above code checks the OS type and if it is either Android or an iOS
then power saving features are deactivated.
