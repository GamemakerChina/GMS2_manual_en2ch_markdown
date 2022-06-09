#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Sequences/i_sequence_position.png) Set Sequence Position

With this action you can set the position for the given sequence element
in the room. You supply the sequence element ID (as returned by the
action [Create Sequence](Create_Sequence_Element) ), and then the
new X and Y position. If you tick the "relative" checkbox, then the
values given for X and Y will be added to the current sequence position,
otherwise they will be an absolute position.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Sequences/a_sequence_position.png)  

#### Arguments:

|          |                                                        |
|----------|--------------------------------------------------------|
| Argument | Description                                            |
| Variable | The ID of the sequence element to set the position of. |
| X        | The new x position in the room for the sequence.       |
| Y        | The new y position in the room for the sequence.       |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Sequences/e_sequence_position_get.png)  
The above action block code retrieves the current position of the
sequence element ID stored in the variable " my_seq ". These values are
then used to set the position of the sequence, moving it 10 pixels to
the right.
