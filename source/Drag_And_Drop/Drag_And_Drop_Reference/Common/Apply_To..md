#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Common/i_Common_Apply_To.png) Apply To...

This action can be used to change the [Action
Scope](../../Drag_And_Drop_Overview/Applying_Actions_To_Other_Instances)
for all further actions to chained to this one. Like with an
[if](If_Variable) action, if you drop further actions to the right
of the **Apply to...** action then they will be run from the scoped
object or instance. The scope is chosen from the pop up menu shown when
you click the small arrow at the top right of the action, and in this
way you can tell a different set of objects - or even a single instance
if you have the instance ID - to run multiple actions before continuing
with the code of the current object. Note that to add actions into the
"Applies To" block, they should be dropped to the *side* of the action,
as shown in the image below:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Common/Drop_Applies_To.png)  
These actions will now be run from the object or instance that is being
targeted by the "Applies To" block, while any actions dropped elsewhere
will be performed after the "Applies To" block.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Common/a_Common_Apply_To.png)  

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Common/e_Common_Apply_To.png)  
The above action block code checks a variable to see if it equals 100
and if it does it changes scope to the " obj_Player " instances and
tells them to run the [Set Sprite](../Instance/Set_Sprite) action
(all instances of this object in the room will change sprite at this
point), before continuing to add 1 onto the variable within the instance
running the full code block.
