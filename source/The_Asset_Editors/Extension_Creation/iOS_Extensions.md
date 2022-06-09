# iOS / tvOS Extensions

To create an extension for iOS or tvOS you have to do it in two parts.
The first part would be to add the extension itself, along with the
required files, and the second is to create the functions and
macros/constants that the extension requires. The functions and
constants are added using **placeholder** files to group them together,
so you'd add a placeholder and then define the functions and macros as
explained in the section [here](Creating_An_Extension) . To add the
rest of the files though you need to first tick the *iOS* and/or the
*tvOS* check-box in the **Additional Features** section of the editor to
open up the relevant **Extension Properties** window (the image below
shows the iOS properties window, but the tvOS window is exactly the
same):  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Extensions_iOS.png)  
Here you can give the following details:

-   **Compiler Flags / Linker Flags** : Some frameworks and third party
    SDKs require the addition of extra linker flags and compiler flags
    to work, which can be specified here (see the documentation that
    accompanies the SDK or framework in question for details).

-   **Class Name** : Your extension can have multiple classes, with each
    class having its own functions and constants, so you should give it
    a name that reflects its purpose.

-   **App Delegate Class Name** : The name of your custom app delegate
    class. Setting this allows the extension to override/extend core app
    functionality. To use this feature you need to do the following:

    1.  Ensure that the delegate source files have the same name as the
        delegate class (e.g. @interface MyCustomAppDelegate should be
        defined in " MyCustomAppDelegate.h ")
    2.  Add the ${YYExtAppDelegateIncludes} environment variable at the
        top of your app delegate header file. This will be replaced at
        compile-time with the relevant include files for the parent
        delegate class.
    3.  Use the ${YYExtAppDelegateBaseClass} environment variable as the
        base class for your custom app delegate. This will be replaced
        at compile-time with the correct base delegate class. To ensure
        your extension works with any other extensions that use custom
        app delegates, you should call any base class methods from
        overridden methods in your child class. Before calling the
        superclass method, you need to make sure it is implemented in
        the class hierarchy to avoid errors, for e.g.:

    ``` gml
    - (BOOL)application:(UIApplication *)application willFinishLaunchingWithOptions:(NSDictionary *)launchOptions
    {
        // Check if any superclasses implement this method and call it
        if([[self superclass] instancesRespondToSelector:@selector(application:willFinishLaunchingWithOptions:)])
          return [super application:application willFinishLaunchingWithOptions:launchOptions];
        else
            return TRUE;
    }
    ```

-   **System Frameworks** : Here you can add in any iOS system framework
    s to your extension. These are added by clicking the  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_AddArgument.png)  
    button which will add a placeholder framework, which you can then
    edit by double clicking  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
    on it. You can find out more about available system frameworks
    [here](https://developer.apple.com/documentation/) . To remove a
    system framework, simply select it and then click the  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RemoveArgument.png)  
    button.  
    ![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Extensions_iOS_Weak_Reference.png)  
    You can enable the checkbox for a framework to mark it as a " **Weak
    Reference** ". This adds it to " **Build Phases -\> Link Binary with
    Libraries** " section of Xcode as an " **Optional** " framework, as
    opposed to a " **Required** " framework (which is the default
    behaviour).

-   **3rd Party Frameworks + Bundles** : This section is for adding
    third party and SDK bundles. As with system frameworks you click
    the  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_AddArgument.png)  
    button to add them and then double click  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
    to edit, and selecting them then clicking  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RemoveArgument.png)  
    will remove them (see the documentation that came with your chosen
    SDK for info on the framework name). Here you can choose to **Not
    Embed** the framework, **Embed & Sign** it, or **Embed it without
    Signing** :  
    ![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Extensions_iOS_Embed_Framework.png)  
    This reflects the same option for a framework added under "
    **Frameworks, Libraries and Embedded Content** " in Xcode.

-   **Enter framework path on Mac** : If you want to add a framework to
    the extension whose files are present on the Mac that is used to
    build your project, you can enter the path to that framework (on the
    build machine) into this field and then click the  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_AddArgument.png)  
    button to add it. The path needs to point to a .framework file which
    will be compressed as a .zip and placed into the iOSSourceFromMac
    folder under your extension directory; you can easily open that at
    any time by right clicking  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RMB.png)  
    on the extension and selecting *Open in Explorer* .

-   **Add Source** : You can use this to add the source files required
    for your extension to work. Added files will be stored in the
    iOSSource folder inside your extension directory.

-   **Code Injection** : Here you can add any code to be injected
    (added) into your iOS application when your game is built for
    testing or final release. Make sure to revise this (and your
    permissions) carefully before submitting any games to the store, as
    incorrect settings will cause your game to be failed for submission.

## Code Injection

Code Injection can be used for iOS/tvOS extensions in the same way as
described on the Android Extensions page: see [Code
Injection](Android_Extensions#h) . The following tags are available
for the iOS and tvOS platforms:

``` gml
YYIosPlist
YYIosEntitlements
YYIosCocoaPods
YYIosCocoaPodsDependencies
YYIosBuildRules
YYIosBuildSettingsInjection
YYIosScriptPhase
YYIosCFBundleURLSchemesArray
YYIosLSApplicationQueriesSchemesArray

YYTvosPlist
YYTvosEntitlements
YYTvosCocoaPods
YYTvosCocoaPodsDependencies
YYTvosBuildRules
YYTvosBuildSettingsInjection
YYTvosScriptPhase
YYTvosCFBundleURLSchemesArray
YYTvosLSApplicationQueriesSchemesArray
```

The runtime location where the code is injected will depend on the type
of the tag:

|                       |                                                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| Tag Type              | Injection Path                                                                                                    |
| **Entitlements**      | {RUNTIME}\ios\TemplateProject\\${YYXCodeProjName}\\ ${YYXCodeProjName}.entitlements                               |
| **info.plist**        | {RUNTIME}\ios\TemplateProject\\${YYXCodeProjName}\\ Supporting Files\\ ${YYXCodeProjName}-Info.plist              |
| **infoPlist.strings** | {RUNTIME}\ios\TemplateProject\\${YYXCodeProjName}\\ en.lproj\InfoPlist.strings                                    |
| **project.pbxproj**   | {RUNTIME}\ios\TemplateProject\\${YYXCodeProjName}.xcodeproj\\ project.pbxproj                                     |
| **xcscheme**          | {RUNTIME}\ios\TemplateProject\\${YYXCodeProjName}.xcodeproj\\ xcshareddata\xcschemes\\${YYXCodeProjName}.xcscheme |

NOTE These paths are only for VM. For YYC, injected code will go into
the {RUNTIME}\yyc\\ directory, where the paths may or may not be
equivalent to those for VM. Note that there is a Game Option [for
iOS](../../Settings/Game_Options/iOS) and [for
tvOS](../../Settings/Game_Options/tvOS) to add a Podfile.lock file
to GameMaker , which is required if you are adding CocoaPods
Dependencies in this section.

## Additional Information

If your extension has had any System Frameworks or 3rd Party Frameworks
added, these will now be listed in the **Extension Properties** window,
with each one having a check-box beside it. If you mark the check-box,
you are enabling weak linking, which is useful should you need to
"override" any symbol from the included library with your own value, but
it should be noted that doing so will slow linking down. For information
on your creating native extensions for iOS, see [Source
Examples](Extended_Examples) ; and for information on using
CocoaPods in extensions, see the following guide:

-   [iOS and tvOS: Using Cocoa
    Pods](https://help.yoyogames.com/hc/en-us/articles/360008958858)
