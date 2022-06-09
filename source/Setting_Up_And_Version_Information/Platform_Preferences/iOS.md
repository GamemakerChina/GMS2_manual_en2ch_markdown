# iOS Preferences

The iOS preferences have the following options:  
![](https://gms.magecorn.com/Manual/assets/Images/Setup_And_Version/Platform_Preferences/iOS_Prefs.png)  

-   **Suppress build and run** : By default when you create an iOS
    project and then build a final executable package, GameMaker will
    build the package and then attempt to run it on any connected
    devices. Checking this option will suppress building the app and
    running it on the device and simply create an XCode project on the
    host Mac
-   **macOS Install Path** : The install path for the project files on
    the build Mac.
-   **Default Team Identifier** : Here you can add your default Team
    Identifier, [as assigned to you by
    Apple](https://help.apple.com/xcode/mac/current/#/dev23aab79b4) .
    This Team Id will be used when your game files are sent to Xcode to
    build the app, and will permit Xcode to generate the required
    signing certificates. Note that this setting will be applied by
    default to all games built for iOS, but it can be over-ridden on a
    per-project basis from the General iOS [Game
    Options](../../Settings/Game_Options/iOS) .
