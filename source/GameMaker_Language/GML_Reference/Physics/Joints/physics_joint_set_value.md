# physics_joint_set_value

Certain joint properties can be changed and set even after the creation
of the joint. There are a number of constants that can be used in this
function and they can be found here: [Physics Joint
Constants](Physics_Joint_Constants) .

#### Syntax:

``` gml
physics_joint_set_value(joint, field, value)
```

|          |                                                                                                                        |                                                             |
|----------|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Argument | Type                                                                                                                   | Description                                                 |
| joint    |  [Physics Joint ID](../../../../../GameMaker_Language/GML_Reference/Physics/Joints/Joints)                         | The index of the joint that you wish to change              |
| field    |  [Physics Joint Constant](../../../../../GameMaker_Language/GML_Reference/Physics/Joints/Physics_Joint_Constants)  | The constant for the joint property that you wish to change |
| value    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                 | The new value for the joint property                        |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if physics_joint_get_value(revJoint, phy_joint_max_motor_torque) &amp;lt; 2
{
    physics_joint_set_value(revJoint, phy_joint_max_motor_torque, 2);
}
```

The above code checks to see if the joints maximum motor torque is set
to less than 2 and if it is it then sets it to 2.
