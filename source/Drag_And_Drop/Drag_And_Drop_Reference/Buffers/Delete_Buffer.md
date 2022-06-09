#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Buffers/i_Buffers_Delete_Buffer.png) Delete Buffer

This action can be used to delete a buffer from memory, releasing the
resources used to create it and removing any data that it may currently
contain. You supply the unique buffer ID value as returned by the action
[Create Buffer](Create_Buffer) . Note that you can select multiple
buffers for removal by clicking the plus icon   
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Icon_Expand_Arguments.png)  
beside the action, and adding another buffer ID. **NOTE** : It's
important to always remove any dynamically created resources from memory
when you no longer need them to prevent memory leaks.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Buffers/a_Buffers_Delete_Buffer.png)  

#### Arguments:

|          |                                         |
|----------|-----------------------------------------|
| Argument | Description                             |
| Buffer   | The buffer index (stored in a variable) |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Buffers/e_Buffers_Delete_Buffer.png)  
The above action block code checks to see if a buffer exists and if it
does it is deleted.
