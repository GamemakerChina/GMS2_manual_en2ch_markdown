#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Sequences/i_sequence_pause.png) Play Sequence

With this action you can pause a playing sequence. You supply the
sequence element ID (as returned by the action [Create
Sequence](Create_Sequence_Element) ), and the action will pause it
playing.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Sequences/a_sequence_pause.png)  

#### Arguments:

|          |                                          |
|----------|------------------------------------------|
| Argument | Description                              |
| Variable | The ID of the sequence element to pause. |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Sequences/e_sequence_play.png)  
The above action block code checks to see if a global variable is true .
If it is then the sequence element referenced in the variable " my_seq "
is paused, otherwise it is set to play.
