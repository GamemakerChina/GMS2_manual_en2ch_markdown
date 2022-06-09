# physics_joint_get_value

By using a series of predefined constants, you can ask GameMaker to tell
you a number of things about the state of any given joint. This is very
useful as it gives you the ability to delete joints or change an
instances behaviour depending on whatever your needs are at the time.
There are a number of constants that can be used in this function and
they can be found here: [Physics Joint
Constants](Physics_Joint_Constants) , but be aware that complex
calculations are done when you call these, so they should be used with
care and only when necessary and note that *many are unique to a
specific type of joint* . If the property does not exist (if, for
example, you check a pulley joint for prismatic translation) then 0 will
be the return value.

#### Syntax:

``` gml
physics_joint_get_value(joint, value)
```

|          |                                                                                                                        |                                                           |
|----------|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Argument | Type                                                                                                                   | Description                                               |
| joint    |  [Physics Joint ID](../../../../../GameMaker_Language/GML_Reference/Physics/Joints/Joints)                         | The index of the joint that you wish to test              |
| value    |  [Physics Joint Constant](../../../../../GameMaker_Language/GML_Reference/Physics/Joints/Physics_Joint_Constants)  | The constant for the joint property that you wish to test |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if shipJoint
{
    var reactionForceX = physics_joint_get_value(shipJoint, phy_joint_reaction_force_x);
    var reactionForceY = physics_joint_get_value(shipJoint, phy_joint_reaction_force_y);
    var reactionForce = point_distance(0, 0, reactionForceX, reactionForceY);
    if reactionForce &amp;gt; 2
    {
        physics_joint_delete(shipJoint);
        shipJoint = -1;
    }
}
```

The above code checks to see if the variable "shipJoint" holds a joint
index and if it does, it then calculates the force being applied to that
joint using the two constants. Finally, if the total force is greater
than 2, the joint is deleted.
