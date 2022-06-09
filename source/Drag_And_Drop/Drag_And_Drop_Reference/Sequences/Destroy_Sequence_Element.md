#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Sequences/i_sequence_destroy.png) Destroy Sequence

You can call this action whenever you wish to "destroy" a previously
created sequence element. You give the element ID, as returned by the
action [Create Sequence Element](Create_Sequence_Element) , and this
action will destroy it, removing it from the room.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Sequences/a_sequence_destroy.png)  

#### Arguments:

|          |                                            |
|----------|--------------------------------------------|
| Argument | Description                                |
| Variable | The ID of the sequence element to destroy. |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Sequences/e_sequence_exists.png)  
The above action block code checks for to see if the sequence element
stored in the variable " my_seq " exists and if it does, it then
destroys it.
