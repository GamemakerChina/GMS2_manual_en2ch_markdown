#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Sequences/i_sequence_get_length.png) Get Sequence Length

With this action you can retrieve the length (in frames) of the given
sequence element in the room. You supply the sequence element ID (as
returned by the action [Create Sequence](Create_Sequence_Element) ),
and this action will return its length in the target variable. This will
be the number of frames that the Sequence runs for. Note that the target
variable can be flagged as temporary (local), which will be created for
the action and can be used in all subsequent actions for the event the
action is in.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Sequences/a_sequence_get_length.png)  

#### Arguments:

|          |                                                      |
|----------|------------------------------------------------------|
| Argument | Description                                          |
| Variable | The ID of the sequence element to get the length of. |
| Target   | The target variable to hold the length.              |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Sequences/e_sequence_length.png)  
The above action block retrieves the length of the sequence element ID
stored in the variable " seq_id ". That value is then used to set the
head position of the same sequence element to 10 frames before its end.
