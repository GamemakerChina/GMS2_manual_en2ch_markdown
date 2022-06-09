#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Sequences/i_sequence_exists.png) If Sequence Exists

This action can be used to check if the given sequence element exists in
the game room. You give the element ID, as returned by the action
[Create Sequence](Create_Sequence_Element) , and if the sequence
element exists in the room then the action will return true otherwise it
will return false . If you flag the " **Not** " argument, then the
action will check to see if *no* such sequence element exists and if
none are found it will return true . Note that to add actions into the "
if " block, they should be dropped to the side of the action, as shown
in the image below:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Sequences/a_sequence_exists_drop.png)  
These actions will now be run if the " if " evaluates to true , while
any actions dropped elsewhere will be performed after the " if " block.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Sequences/a_sequence_exists.png)  

#### Arguments:

|          |                                                  |
|----------|--------------------------------------------------|
| Argument | Description                                      |
| Sequence | The element ID of the sequence element to check. |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Sequences/e_sequence_exists.png)  
The above action block code checks for to see if the sequence element
stored in the variable " my_seq " exists and if it does, it then
destroys it.
