# Android Extensions

To create an extension for Android you have to do it in two parts. The
first part would be to add the extension itself, along with the required
files, and the second is to create the functions and macros/constants
that the extension requires. The functions and constants are added using
**placeholder** files to group them together, so you'd add a placeholder
and then define the functions and macros as explained in the previous
section. To add the rest of the files though you would need to first
tick the *Android* check-box in the **Extra Platforms** section of the
editor, which will open up the extension's Android Properties:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Extensions_Android.png)  
Here you can give the following details:

-   **Class Name** : Your extension can have multiple classes, with each
    class having its own functions and constants, so you should give it
    a name that reflects its purpose.
-   **Android Permissions** : Here you can add in any extra permissions
    that your extension requires. What these permissions are will depend
    entirely on the use that the extension has, and so you should [check
    the documentation supplied by
    Google](https://developer.android.com/reference/android/Manifest.permissionl)
    for the Android platform, or, if you are using a third party SDK,
    the documentation that comes with the SDK. To add a new permission
    you need to click on the  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_AddArgument.png)  
    button to add a placeholder permission, and then do a double  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
    click on that to edit it to what is required. You can remove
    permissions using the  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RemoveArgument.png)  
    button.
-   **Code Injection** : Here you can add any code to be injected
    (added) into your Android application when your game is built for
    testing or final release. Make sure to revise this (and your
    permissions) carefully before submitting any games to the store, as
    incorrect settings will cause your game to be failed for submission.
    See the section below for more information.

## Code Injection

Any code entered into the "Code Injection" window will need to be
separated into distinct XML groups, as shown in the screenshot above.
The XML tag you use for a group will determine where the code is
injected into your application. You can use the following syntax to
create code injection groups:

``` gml
&amp;lt;YYTagName&amp;gt;

// Code to inject

&amp;lt;/YYTagName&amp;gt;
```

The following tags are available for the Android platform:

``` gml
YYAndroidTopLevelGradle
YYAndroidTopLevelGradleBuildscript
YYAndroidTopLevelGradleBuildscriptRepositories
YYAndroidTopLevelGradleBuildscriptDependencies
YYAndroidTopLevelGradleAllprojects
YYAndroidTopLevelGradleAllprojectsRepositories
YYAndroidTopLevelGradleEnd

YYAndroidGradle
YYAndroidGradleEnd
YYAndroidGradleAndroid
YYAndroidGradleDependencies 
YYAndroidGradleProperties
YYAndroidManifestAttributes
YYAndroidManifestApplicationAttributes
YYAndroidManifestActivityAttributes
YYAndroidManifestActivityInject
YYAndroidManifestApplicationInject
YYAndroidStringValuesInjection
YYAndroidLayout
```

The runtime location where the code is injected will depend on the type
of the tag:

|                         |                                                                       |
|-------------------------|-----------------------------------------------------------------------|
| Tag Type                | Injection Path                                                        |
| **Top Level Gradle**    | {RUNTIME}\android\runner\RootFiles\build.gradle                       |
| **Module Level Gradle** | {RUNTIME}\android\runner\ProjectFiles\build.gradle                    |
| **Android Manifest**    | {RUNTIME}\android\runner\ProjectFiles\src\main\AndroidManifest.xml    |
| **Strings**             | {RUNTIME}\android\runner\ProjectFiles\src\main\res\values\strings.xml |
| **Layout**              | {RUNTIME}\android\runner\ProjectFiles\src\main\res\layout\main.xml    |

**NOTE** : These paths are only for VM; for YYC, injected code will go
into the {RUNTIME}\yyc\\ directory, where the paths may or may not be
equivalent to those for VM.

## Source Files

Once you have set this up correctly, you will need to add the files
required for your extension package to work. To do this you need to
click on the buttons at the bottom, either *Add SDK* or *Add Source* and
then browse to the files you wish to add. Added files will be stored in
the AndroidSource directory along with your extension. You can open this
location at any time by right clicking  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RMB.png)  
on the extension and selecting *Open in Explorer* . For information on
your creating native extensions for Android, see [Source
Examples](Extended_Examples) .
