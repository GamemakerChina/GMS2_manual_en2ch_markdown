#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Mouse_And_Keyboard/i_VirtualKeyboard_Hide.png) Hide Virtual Keyboard

This action can be used to hide the virtual keyboard on the device
running the game. Calling this action will generate a [System
Asynchronous
Event](../../../The_Asset_Editors/Object_Properties/Async_Events/System)
, in which the
[async_load](../../../GameMaker_Language/GML_Overview/Variables/Builtin_Global_Variables/async_load)
[DS
map](../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/DS_Maps)
will be populated with the following key/value pairs:

-   " **event_type** " - this will be " **virtual keyboard status** "
    when triggered by virtual keyboard actions.
-   " **screen_height** " - the height of the virtual keyboard (in
    pixels). This will be 0 if the keyboard is invisible.
-   " **keyboard_status** " - the current status of the keyboard,
    returned as one of the following strings:
    -   "hiding"
    -   "hidden"
    -   "showing"
    -   "visible"

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Mouse_And_Keyboard/a_VirtualKeyboard_Hide.png)  

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Mouse_And_Keyboard/e_VirtualKeyboard_Show.png)  
The above action block code checks for a mouse down action, and if one
is detected, then a check is performed to see if the OS virtual keyboard
is showing. If it isn't then it is set to show - using a numeric keypad
type - and if is already showing then it is hidden.
