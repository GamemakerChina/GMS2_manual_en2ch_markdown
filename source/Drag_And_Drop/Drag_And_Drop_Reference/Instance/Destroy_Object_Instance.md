#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/i_Instance_Destroy.png) Destroy Object Instance

You can call this action whenever you wish to "destroy" an instance,
which will remove it from the room. You should note that when you
destroy an instance, its [Destroy
Event](../../../The_Asset_Editors/Object_Properties/Object_Events)
is called *immediately after the action that calls the destroy* . Also
note that although the Destroy Event is performed the instant that the
action is called, the instance is *not* immediately removed from the
game, and it will continue to perform the code contained in the current
event until the end, and only when the current event is over will the
instance be removed from the game, at which time the [Clean Up
Event](../../../The_Asset_Editors/Object_Properties/Object_Events)
will be called.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/a_Instance_Destroy.png)  

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Instance/e_Instance_Destroy.png)  
The above action block code checks for a collision with any other
instance at the position of the calling instance, and if one is found,
it destroys itself.
