#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/i_Instance_Call_Event.png) Call Parent Event

This action block will perform the event of the parent object that the
instance is a child of before continuing to run the actions in the
actual instance. When you assign a parent object to an instance, all the
events from that object are "inherited" by the child. However if you
then add an event to the child object, it overrides the parent event.
Using this action block, you can force a child object to run both the
parent event and the event in the instance itself. See the [Object
Editor](../../../The_Asset_Editors/Objects) section for more
information on parents.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/a_Instance_Call_Event.png)  

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/e_Instance_Call_Event.png)  
The above action block code calls the parent event of the object that
the instance is a child of and then sets an alarm and changes the
sprite.
