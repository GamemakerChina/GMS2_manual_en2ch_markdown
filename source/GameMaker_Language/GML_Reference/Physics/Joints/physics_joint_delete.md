# physics_joint_delete

Once two instances with physics representations have been bound by a
joint, this can be deleted again at any time. Normally this will happen
automatically when one of the two instances is destroyed, or when the
room ends, but there are times when you may wish to do this manually. In
those cases you would use this function. It should also be noted that
whenever an instance that is part of a [gear
joint](physics_joint_gear_create) is destroyed, the gear joint
should be deleted using this function *before* any of the instances
involved in forming the gear (but the remaining joints will be deleted
automatically), for example in the destroy event of the instance.

#### Syntax:

``` gml
physics_joint_delete(joint)
```

|          |                                                                                                 |                                                |
|----------|-------------------------------------------------------------------------------------------------|------------------------------------------------|
| Argument | Type                                                                                            | Description                                    |
| joint    |  [Physics Joint ID](../../../../../GameMaker_Language/GML_Reference/Physics/Joints/Joints)  | The index of the joint that you wish to delete |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var reactionForceX, reactionForceY, reactionForce;
if shipJoint
{
    reactionForceX = physics_joint_get_value(shipJoint, phy_joint_reaction_force_x);
    reactionForceY = physics_joint_get_value(shipJoint, phy_joint_reaction_force_x);
    reactionForce = sqrt((reactionForceX + reactionForceX) + (reactionForceY + reactionForceY));
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
