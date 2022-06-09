# Redefine Keys Preferences

  
![](https://gms.magecorn.com/Manual/assets/Images/Setup_And_Version/Preferences/Redefine_Keys_Preferences.png)  
The **Redefine Keys** section of the Preferences allows you to change
the mappings for the various [keyboard
shortcuts](../../IDE_Navigation/Keyboard_Shortcuts) provided in the
GameMaker IDE.

## Search

At the top you have the search bar, which you can use to look for
specific commands by entering a name (e.g. " **Copy** "), a key
combination (e.g. " **CTRL+C** ") or a location (e.g. " **Text Editor**
"). Enabling the  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Redefine_Keys_Search_Side_Button.png)  
button next to the search field allows you search by entering a
shortcut. Any keys you press while this is enabled will be entered as a
shortcut instead of regular text.  
![](https://gms.magecorn.com/Manual/assets/Images/Setup_And_Version/Preferences/Redefine_Search_Modes.gif)  
Next to the search bar you have the **Filter** menu which is described
in its own section later on this page.

## Command List

The "Command List" displays all the available shortcuts that can be
remapped, separated into different categories based on the locations of
those shortcuts. Clicking on any location in this list will display the
commands that can be used within it:  
![](https://gms.magecorn.com/Manual/assets/Images/Setup_And_Version/Preferences/Redefine_Keys_Preferences_Expanded.png)  
Information for each command is separated into two columns:

-   **Command** : This is the name of the command/shortcut and describes
    what action it performs.

-   **Keys** : This displays the current keyboard mapping for the
    command. You can  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
    double click on any item in this column to reassign that command by
    simply pressing the appropriate combination of keys on the keyboard
    (they must be held simultaneously, similar to how the shortcut would
    actually be used). As soon as you release your new key combination,
    it will be registered and applied to the command.

    ![Double-click on a shortcut to enter a new
    one!](https://gms.magecorn.com/Manual/assets/Images/Setup_And_Version/Preferences/Redefine_Example.gif)

    Pressing  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Escape.png)  
    while editing a command will bring you out of edit mode and will not
    modify the selected command.

You can change the sorting of the Command List by  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
clicking on a column heading (either "Command" or "Keys") to sort the
list using the values from that column, alternating between ascending
and descending with each click.

## Clash Window

If you try to set a key combination that is already in use for other
commands, you will see a special "Clash" window:  
![](https://gms.magecorn.com/Manual/assets/Images/Setup_And_Version/Preferences/Redefine_Keys_Clash_Window.png)  
This window will show the location and name of the command that is
already using the key combination that you are trying to use. In case
the key combination is used by multiple commands, it will show all of
them in a list. Here you have two options, **"Cancel"** and **"Override
(ALL) and Reassign"** :

-   Pressing **"Cancel"** will close the Clash window and will not make
    any changes to any commands.
-   Pressing **"Override (ALL) and Reassign"** will assign the new key
    combination to your selected command and **clear** the bindings of
    all other commands that previously used the same combination.

After using **"Override and Reassign"** , GameMaker will highlight the
overridden command in the Command List so you can assign new a key
combination to it. In case multiple commands were overridden, it will
change the filter to display only those commands so you can apply new
shortcuts to them. This filter can be cleared by clicking on "Clear". If
you wish to use a different binding for the selected command, you can
expand the **"Suggested Free Keys"** section to see a list of key
combinations that are not used anywhere in the IDE. Clicking on
**"Use"** next to any one of these combinations will assign it to the
selected command and solve the clash.

## Filter Menu

  
![](https://gms.magecorn.com/Manual/assets/Images/Setup_And_Version/Preferences/Redefine_Keys_Filter_Menu.png)  
The Filter menu allows you specify what kind of commands should appear
in the Command List. At the top, you have two options:

-   **"Show Unbound Commands"** : Enabling this will display any
    commands that have been unbound, i.e. their bindings have been
    cleared. Any commands that remain unbound cannot be used as there is
    no key combination assigned to them.
-   **"Show Only Redefined Commands"** : Enabling this will display only
    those commands that have been changed manually, i.e. their bindings
    are different from their default bindings.

Below that you have numerous options allowing you to specify the
locations that are displayed in the Command List. By default, **"All
Locations"** is checked, meaning that you will see commands from all
locations in the IDE. Unchecking **"All Locations"** will uncheck every
other item below it, allowing you to manually select the ones you would
like to see; for example, unchecking all items and then checking
**"Image Editor"** will only show you commands that can be used in the
Image Editor.

## Clearing Commands

Double-clicking on an existing key combination will allow you to change
it, however while you are doing this you can click on the **"Clear"**
button below the Command List to clear the binding for that command.  
![](https://gms.magecorn.com/Manual/assets/Images/Setup_And_Version/Preferences/Redefine_Clear_Button.png)  
If you have accidentally overridden some keyboard shortcuts and wish to
reset them back to their default settings, you can click on the "Restore
defaults" button at the top of the Preferences window to reset all
commands to their default mappings, or check the [Keyboard
Shortcuts](../../IDE_Navigation/Keyboard_Shortcuts) page to check
the default bindings and revert your commands manually.
