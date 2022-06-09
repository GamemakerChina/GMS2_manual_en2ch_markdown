# uwp_license_trial_version

This function can be used to check whether the game is under a trial
licence or not. If it is the function will return true , or false
otherwise.

#### Syntax:

``` gml
uwp_license_trial_version();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if uwp_license_trial_version()
{
    global.LevelCap = 10;
}
```

The above code checks to see if the app is under a trial licence and, if
so, it sets a global variable.
