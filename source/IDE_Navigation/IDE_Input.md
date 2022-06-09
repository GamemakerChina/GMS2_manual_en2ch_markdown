# IDE Input And Navigation

The GameMaker IDE accepts mouse and keyboard input, and many operations
can be carried out using one or the other or both. In general you can
click the left mouse button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
to select anything, use  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
/  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
+  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
to select multiple items, hold  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
to drag items into different docks or onto the workspaces, and also
the  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RMB.png)  
to open context specific menus. Note that if you are running GameMaker
on a macOS system and are using a single button mouse, please use  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
+  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
to get a right mouse click  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RMB.png)  
. There are also a great number of keyboard shortcuts that can be used
to navigate around the different workspace elements and resource
editors, and we'll quickly go through some of the most important ones
(you can find a complete list [here](Keyboard_Shortcuts) ):

-     
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
    /  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
    + "Z" : This will undo the previous action and works in most of the
    editors. You have multiple levels of undo too, so you can press this
    multiple times to "roll back" changes.
-     
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
    /  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
    + "Y" : This will redo a previous action that was undone and works
    in most of the editors. Like undo, you have multiple levels of redo
    too.
-     
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
    /  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
    + "S" : This will force GameMaker to save your project.
-     
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
    /  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
    + "T" : This will open the **Goto Window** which enables you to
    quickly search for and go to any asset in your game, as well as
    search the
    [Preferences](../Setting_Up_And_Version_Information/IDE_Preferences)
    and [Game Options](../Settings/Game_Options) . You are presented
    with a list of everything and as you type the search term, this list
    will be culled to suit, so if all your rooms are prefixed with
    "rm\_" for example, typing that will cull the list to show only
    those assets that begin with that name.

  
![](https://gms.magecorn.com/Manual/assets/Images/Introduction/QS_Goto.png)  

-     
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
    /  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
    +  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Tab.png)  
    : This will open the **Workspace Overview** window which can be used
    to navigate quickly between items that are open in the different
    workspaces. The window will remain open as long as  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
    or  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
    is held, and pressing  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Tab.png)  
    once will move you to the next item in the window. Releasing the
    shortcut will then navigate to the item that was selected. NOTE If
    you remap the binding for this window to either use more than one
    modifiers (such as  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
    +  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Alt.png)  
    + B ) or a single key (such as B only), then the window will remain
    open after pressing the shortcut regardless of whether you still
    have it held or not, until you manually close it or choose an item
    from the window.

  
![](https://gms.magecorn.com/Manual/assets/Images/IDE_Input/Getting_Started_Overview.png)  

-     
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_f1.png)  
    : This will open the manual. Note that when using GML Visual or GML
    code you can also select an action or a function (or keyword or
    whatever) and then press  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_f1.png)  
    or click the middle mouse button  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_MMB.png)  
    to open the manual on the relevant page.
-     
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_f12.png)  
    : This can be used to collapse or expand all the different docked
    windows in the IDE.

Other ways to navigate the workspace include using the keyboard
shortcut  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
/  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
+  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Alt.png)  
+ ** ** to move between any open windows in the direction pressed, and
by pressing and holding the middle mouse button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_MMB.png)  
then dragging the mouse you can pan around the workspace too. When
navigating around the various different workspaces and windows, you can
use the right-mouse button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RMB.png)  
on any text field to open a context menu which will have the following
fields by default:  
![](https://gms.magecorn.com/Manual/assets/Images/Introduction/QS_RMBContextMenu.png)  
In some situations, these options may be expanded on, depending on the
editor or window that is in focus. Other than those methods of input,
there is also limited support for pen devices, and also a special mode
for those people working on projects using a laptop. Both of these are
explained below: [ Laptop Mode Laptop Mode ](#) If you are using
GameMaker on a laptop, then you will have a further option at the top of
the IDE for Laptop Mode:  
![](https://gms.magecorn.com/Manual/assets/Images/IDE_Input/Getting_Started_LaptopMode.png)  
This will be on by default but can be switched off if you prefer by
toggling this button. Laptop mode combines with some tools in the IDE to
make it a much better experience when using a touchpad, simplifying the
3 main mouse interactions: **Pan** , **zoom** and **scroll** . It uses
two modifier keys to do this: Left  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
/  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
and Left  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Alt.png)  
. When laptop mode is on, *Left*  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
/  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
and *Left*  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Alt.png)  
are "reserved" for mouse interactions like panning the room editor,
where *Left*  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
/  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
is zoom, *Left*  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Alt.png)  
is scroll and pan. Scrolling in laptop mode behaves just like panning,
so it should be intuitive and precise enough so that you don't need to
use the scrollbar. Note that when holding these buttons, you simply have
to move the mouse - not click nor drag, just move - and that if there is
a general shortcut that normally requires the use of the  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
/  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
or  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Alt.png)  
keys, you would use the *Right* keys of the keyboard instead. [ Touch
Screen Support Touch Screen Support ](#) One final thing we'll mention
here is that the IDE for GameMaker also has minimal support for touch
screens. On all operating systems you can use the touch screen to click
and drag items in the main workspace, and we support 2 simultaneous
pointers, where a second tap will perform a right-click. Note that on
Windows 8 and above, the GameMaker IDE will support pen devices too. The
following pages contain more detailed and specific information on
navigating the IDE, as well as information on some navigation tools
available to you:

-   [Bookmarks](Bookmarks)
-   [Recent Windows](Recent_Windows)
-   [The Inspector](../IDE_Tools/The_Inspector)
-   [Menus](Menus)
-   [Keyboard Shortcuts](Keyboard_Shortcuts)

You can also find some extra preferences related to the IDE input here:

-   [Input
    Preferences](../Setting_Up_And_Version_Information/IDE_Preferences/General/Input)
