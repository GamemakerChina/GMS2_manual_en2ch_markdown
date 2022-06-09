# os_get_config

This function returns the name (as a string) of the currently selected
configuration for your game. For more information on configurations
please see the section
[Configurations](../../../Settings/Configurations) .

#### Syntax:

``` gml
os_get_config()
```

#### Returns:

``` gml
 String
```

#### Example:

``` gml
if os_get_config() = "Free_Version"
{
    global.Ads = true;
}
else global.Ads = false;
```

The above code will check to see which configuration is being used and
if it is the one called "Free_Version", ads will be enabled in the game.
