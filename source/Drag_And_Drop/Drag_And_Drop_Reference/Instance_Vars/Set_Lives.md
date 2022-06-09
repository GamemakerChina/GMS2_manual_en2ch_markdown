#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance_Vars/i_IV_Set_Lives.png) Set Lives

With this action you can create or set an instance variable for lives.
You supply the value to either set the lives variable to or to add to
the lives variable (if you tick the *relative* checkbox then the value
will be added to the current "lives" value). Note that unlike regular
instance variables the variable name for "lives" is stored internally so
to retrieve the score value you need to use the action [Get
Lives](Get_Lives) .

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance_Vars/a_IV_Set_Lives.png)  

#### Arguments:

|          |                                                                                     |
|----------|-------------------------------------------------------------------------------------|
| Argument | Description                                                                         |
| Lives    | The amount to set the lives to (or to add on to the lives if *relative* is checked) |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance_Vars/e_IV_Set_Score.png)  
The above action block code will check to see if the room is the first
in the game and if it is it sets up "score", "lives" and "health"
variables for the instance.
