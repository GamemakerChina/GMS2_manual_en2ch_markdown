#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Switch/i_Switches_Default.png) Default

This action will create a new **Default** case within a
[Switch](Switch) . The Default case is one that will be performed if
the input value does not match any other case constants. Actions that
are added to a Default case should be dropped to the side of the action,
much as you would add an action to an "if":  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Switch/Default_Drop.png)  

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Switch/a_Switches_Default.png)  

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Switch/e_Switches_Default.png)  
The above action block code gets the value stored in a global variable
and then compares it to the different possible cases. If any one of the
cases is the same as the value, then the action under that case will be
performed, otherwise the next case will be evaluated. If no case matches
the input value, the default case will be run instead.
