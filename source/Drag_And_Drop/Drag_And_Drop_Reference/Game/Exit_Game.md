#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Game/i_Game_Exit_Game.png) Exit Game

With this action you can end the game, triggering the [Other - Game End
Event](../../../The_Asset_Editors/Object_Properties/Other_Events) .
Note that this does not happen the moment the action is called, but
rather at the end of the current event or script, so any actions that
you have after this action has been called will still run until the end
of the event/script is reached. Please note that this action has the
following restrictions:

-   It will report an error on the **iOS** target as it is against the
    conditions of their marketplace.
-   It will have no effect when called on the **HTML5** and **Windows
    UWP** targets.
-   It will work on **Windows** (including games built for Steam),
    **Android** , **Ubuntu (Linux)** and **Mac** .

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Game/a_Game_Exit_Game.png)  

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Game/e_Game_Exit_Game.png)  
The above action block code will check a global variable and if it
returns true the game will be exited.
