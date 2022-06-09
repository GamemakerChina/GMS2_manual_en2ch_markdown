# Compiling

Compiling your game can mean one of two things: compiling it for
testing, or compiling it to create a final *executable package* for a
specific target platform. This page aims to explain both of those
options in detail.

## Compiling for Testing

Compiling your game for testing can be done by simply pressing the Play
button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_PlayGame.png)  
at the top of the IDE, which will launch the game for testing using the
specified target. You can also run the game in **Debug Mode** by testing
using the Debug button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Debug.png)  
. This will run the game, but also open up the **Debug Window** , where
you can monitor how your game performs and see any issues (see the
section on [Debugging](Debugging) for more information).

## Target Settings

By default GameMaker will run and debug using the built in Virtual
Machine (VM) , which is more or less the same as running on the desktop
OS being used. However GameMaker is a **cross platform engine** and you
can test, debug and compile executable packages of your projects on a
number of different target platforms (the exact platforms available will
depend on the details of your licence). To change the current target
platform you can click  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
on the Targets button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Targets.png)  
to open the **Targets Window** , which will look something like this
(exact details will vary based on your licence type):  
![](https://gms.magecorn.com/Manual/assets/Images/Introduction/QS_TargetList.png)  
At the top, beside the Targets button, you have the current settings
which tells you the platform and the specific settings actually being
used, and then the rest of the window is taken up with the details and
options for all the available targets which you can select to use
instead. Each section of this window is explained below:

[ Platform Platform ](#) This section lists all the available target
platforms. The contents of this list will vary depending on the licence
you have, but will always have at least the "Opera GX" target. To select
a target, simply click  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
on it; this will then update the rest of the options windows to show
different details depending on the platform selected. Specific details
on compiling for each platform are given in the " **Creating A Final
Executable Package** " section below. [ Output Output ](#) Each target
platform can have one or more output formats, the main ones being:

-   **VM** : The VM (Virtual Machine) target uses a generic *runner* for
    each platform and then interprets the code for your game. In general
    this option is used for testing due to its faster build times, but
    it does not offer the same performance boost that using the YYC
    option (if available) offers. You can use this to compile executable
    packages for smaller games or games where performance is not ever
    going to be an issue.
-   **YYC** : The YYC (YoYo Compiler) generates C++ code from your GML
    code, before using the target's C++ compiler to compile it into
    native code for the target platform. It strips out unneeded
    functions and performs a host of other optimisation techniques to
    create a smaller and performance-enhanced executable package. This
    can increase your game's performance by at least two or three times,
    especially on logic-heavy games, and is ideal for those larger or
    CPU-intensive projects. Compile times may take longer and you should
    always clear the compiler cache before building any final complete
    asset package for a target platform. Note that the YYC target may
    require extra tools to be installed for the platform selected,
    otherwise it will not work - you can find further information about
    this from the [YoYo Games Help
    Center](https://help.yoyogames.com/hc/en-us/articles/227860547-GMS2-Required-SDKs)
    as well as on the individual [target
    Preferences](../Setting_Up_And_Version_Information/Platform_Preferences)
    pages detailed in this manual.
-   **JavaScript** : The JavaScript target will only be available for
    specific targets, like the HTML5 target, and sets the game to be
    compiled to pure JavaScript. This uses **ECMAScript 2015** (or ES6)
    for the JS it outputs.

[ Device Device ](#) Certain platforms (like iOS or Android) permit you
to associate one or more devices with GameMaker so that games can
selectively compile to them. Initially, the device list will be empty
and you need to click  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
on the Pencil icon  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Pencil.png)  
to open the **Device Editor** :  
![](https://gms.magecorn.com/Manual/assets/Images/Introduction/QS_DeviceEditor.png)  
Here you can add new devices as well as have GameMaker test for a
connection to any device(s) that may be connected. The exact contents of
this window will depend on the platform specifics (see the section on
the [Device
Manager](../Setting_Up_And_Version_Information/The_Device_Manager)
for exact details for any given platform). Once a device has been found
or added, it will then be shown in this window, like in this example
image for Android:  
![](https://gms.magecorn.com/Manual/assets/Images/Introduction/QS_AddDevice.png)  
The exact procedure and requirements for setting up devices and
troubleshooting issues can be found in the appropriate section of the [
GameMaker Knowledge
Base](https://help.yoyogames.com/hc/en-us/categories/204246668-GameMaker-Studio-2)
. [ Config Config ](#) As explained in the section on
[Configurations](../Settings/Configurations) , you can store certain
details for compiling your game as **Configs** . This section of the
Targets window permits you to have GameMaker automatically select a
specific configuration for a specific target platform. There are also a
number or preferences that can be set to modify and customise the
compile workflow, explained on the following page:

-   [Compiling
    Preferences](../Setting_Up_And_Version_Information/IDE_Preferences/General/Compiling)

## Creating A Final Executable Package

### Overview

You can simply click the Create Executable button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Compile.png)  
in the IDE to start the compiler build or select **Create Executable**
from the [Build Menu](../IDE_Navigation/Menus/The_Build_Menu) .
Either process will start the build process which will depend on the
target platform selected. On the Opera GX target, it will open a special
window allowing you compile and upload your game to GXC; on all other
targets it will open a file explorer window where you can give the final
name that you wish to use for your game executable, before clicking
*Save* to start the compile and build process. Once you have done this,
the necessary files will be generated so that you can distribute it as
you wish. For certain platforms, compiling your game project will
require that you have set up the correct **build tools** (see
[here](../Setting_Up_And_Version_Information/Required_SDKs) ) and
also filled in the appropriate [Platform
Preferences](../Setting_Up_And_Version_Information/Platform_Preferences)
. Depending on your
[licence](https://help.yoyogames.com/hc/en-us/articles/115002637011) ,
you may have the option to build your game via command line, allowing
you to set up continuous integration for your project and streamline
your building and testing process. [See this
page](../Settings/Building_via_Command_Line) for more information on
command line building. **NOTE** Before doing a final build of your
project for release, you should **always clear the Asset Compiler
Cache** (using the "broom" icon  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Clean.png)  
at the top of the IDE). GameMaker will cache many of your game files to
keep compilation speed to a minimum and these can sometimes get
corrupted, so it is safer to clear that cache before doing a release
build. The maximum size of the final game package is 4GB, except for
32-bit Windows, where it's 2GB. See [tips for reducing the final game
size](https://help.yoyogames.com/hc/en-us/articles/4642066783505-How-to-Reduce-Your-Game-s-Size)
.

### Target Formats

Each target option saves to a platform specific format, listed below:

-   **Opera GX** - When compiling for the "Opera GX" target, you will
    see the "Opera GX Packaging" window which will first ask you to sign
    in using your Opera account:  
    ![](https://gms.magecorn.com/Manual/assets/Images/Introduction/Compiling/gx_packaging_1.png)  
    Note that you will not need to sign in here if you have already
    signed into GameMaker using your Opera account. After you have
    signed in, it will start compiling your game and proceed to upload
    it to GXC. You can then click on "Edit Game on Opera" to edit it on
    GXC DevCloud and publish it:  
    ![](https://gms.magecorn.com/Manual/assets/Images/Introduction/Compiling/gx_game_compiled.png)  
    Please refer to [this
    page](https://help.yoyogames.com/hc/en-us/articles/4407217145105) on
    the YoYo Games Helpdesk to learn more about the Opera GX upload
    process, and [this
    page](https://help.yoyogames.com/hc/en-us/articles/4625548722193)
    for information on setting up the YYC export for GXC.
-   **Windows** - Compiling for the general Windows OS will first
    request that you choose between creating an *Installer* or a *Zip*
    package, where the installer will be a single executable that will
    install your game, and the Zip file will be a single \*.zip format
    compressed file with all your game files stored within (the files
    will need extracted for the game to run).  
    ![](https://gms.magecorn.com/Manual/assets/Images/Introduction/QS_Windows_Compile_Options.png)  
    If you check the box marked **Remember Packaging Option** then
    GameMaker will remember the choice for all future compiles (this can
    be reset or changed from the [Windows
    Preferences](../Setting_Up_And_Version_Information/Platform_Preferences/Windows)
    ). You can find out more from the [YoYo Games Help
    Center](https://help.yoyogames.com/hc/en-us/sections/207157668) .
    Please note that the Windows target can compile 32bit *or* 64bit
    executables depending on what you have selected in the [General Game
    Options](../Settings/Game_Options/Windows) .  We **strongly
    recommend that all new projects use the x64 Runtime to create 64bit
    executables** as the 32bit runtime will be getting deprecated and
    removed in the future.
-   **Ubuntu (Linux)** - Compiling for Ubuntu will ask you to choose
    between creating an **.AppImage** or a **.zip** file, containing
    either an x64 or an ARM executable (however AppImage does not
    support ARM). You can find out more from the [YoYo Games Help
    Center](http://help.yoyogames.com/hc/en-us/articles/235186168) .  
    ![](https://gms.magecorn.com/Manual/assets/Images/Introduction/Ubuntu_Exports.png)  
    **.AppImage** is useful for sharing as a package via any
    distributor, while **.zip** is used for uploading to Steam (as it
    uses the Steam Runtime specifically).
-   **HTML5** - If you have chosen to build HTML5, then an indexl
    file (this is the default name, but you can give your own name too
    in the Platform Preferences) along with a folder containing your
    game files will be created and saved to the specified location. For
    your game to work you will need both of these to be uploaded to a
    server . The indexl can also be customised to show your game
    with a different background colour, or at a different position
    etc... but a knowledge of HTML is necessary for this, and you can
    also specify your own custom index file when you build the package
    (see the [HTML5 Game Options](../Settings/Game_Options/HTML5) ).
    You can find out more from the [YoYo Games Help
    Center](http://help.yoyogames.com/hc/en-us/sections/115000309008) .
-   **Android** - For Android devices, you can choose to build an \*.apk
    or an \*.aab (Android App Bundle) file from the window that is shown
    for saving the game:  
    ![](https://gms.magecorn.com/Manual/assets/Images/Introduction/QS_AndroidFileSelector.png)  
    The type of file you choose will depend on the store that you wish
    to target, with the \*.aab file being required for Google Play,
    while the \*.apk file can be used on other stores. You can find out
    more from the [YoYo Games Help
    Center](http://help.yoyogames.com/hc/en-us/articles/115001368727) .
-   **iOS** - Compiling to iOS will create an xarchive file which is
    then used in Xtools to create the final iOS package. Note that **to
    compile for iOS you will require an Apple Mac computer running OSX
    or higher as well as the relevant certificates and permissions** .
    You can find out more from the [YoYo Games Help
    Center](http://help.yoyogames.com/hc/en-us/articles/115001368747) .
-   **macOS** - Compiling for the macOS target will first request that
    you choose between creating a *DMG* or a *Zip* file:  
    ![](https://gms.magecorn.com/Manual/assets/Images/Introduction/QS_macOS_Compile_Options.png)  
    "Package as DMG" will build a .dmg installer package which can be
    used to install the game on a Mac computer. Note that during this
    build process you will see the installer appear on the Mac, which
    will disappear once the build process is complete. "Package as
    Zip" will build either an \*.app file or a \*.pkg file, depending on
    whether you want to later upload it to the Mac App Store or not. As
    with iOS **you will require an Apple Mac computer running OSX or
    higher as well as the relevant certificates and permissions** . You
    can find out more from the [YoYo Games Help
    Center](http://help.yoyogames.com/hc/en-us/articles/235186128) .
-   **Windows UWP** - For Windows UWP, GameMaker will create an
    \*.appxbundle package which can then be uploaded to the Windows
    Store or distributed elsewhere. When you click the Create Executable
    button you will be prompted to tell GameMaker which type of package
    you would like to create (can be for ARM, x64 and/or x86
    architectures ), and you should choose those targets that the game
    will be supported on (you must select at least one, but can select
    all three or any combination):  
    ![](https://gms.magecorn.com/Manual/assets/Images/Introduction/QS_UWP_Compile_Options.png)  
    If you check the box marked **Package For Store Upload** , then the
    final package created will be an \*.appxupload file, which is what
    Microsoft specifies should be used for submitting apps to their
    store, as explained in this article
    [here](https://docs.microsoft.com/en-us/windows/uwp/publish/upload-app-packages)
    (all chosen architectures will be included, just like with the
    \*.appxbundle ). You can find out more about setting up and
    compiling to UWP platform from the [YoYo Games Help
    Center](http://help.yoyogames.com/hc/en-us/sections/115000309028) .

Once you have created your executable asset package you can then give
the file to other people or place it on your website to download, or
upload these files to the different hosting services for individual
distribution or even to online stores (like Google Play, Apple App Store
or the Microsoft Store) for general distribution and retail. Note that
you are free to distribute the games you create with GameMaker in any
way you like, including selling them. Of course, this assumes that the
sprites, images, and sounds you used to make it can be distributed or
sold as well and that you have the legal rights to all assets, and it
also assumes that the game complies with the [YoYo Games EULA for
GameMaker ](https://www.yoyogames.com/legal/eula) .
