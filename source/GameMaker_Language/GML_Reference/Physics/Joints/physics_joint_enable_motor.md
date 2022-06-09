# physics_joint_enable_motor

When you have a joint with a motor (
[prismatic](physics_joint_prismatic_create) or
[revolute](physics_joint_revolute_create) ), you may want to be able
to switch the motor on or off depending on variables and conditions
within the game. For this, you need to have stored the index of the
joint previously in a variable and then you can switch the motor on or
off by using this function and setting the "motor" argument to true or
false .

#### Syntax:

``` gml
physics_joint_enable_motor(joint, motor)
```

|          |                                                                                                 |                                                             |
|----------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Argument | Type                                                                                            | Description                                                 |
| joint    |  [Physics Joint ID](../../../../../GameMaker_Language/GML_Reference/Physics/Joints/Joints)  | The joint that you wish to enable or disable the motor on   |
| motor    |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                       | Whether you wish to turn the motor on (true) or off (false) |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var t_fix = physics_fixture_create();
physics_fixture_set_circle_shape(t_fix, sprite_get_width(sprite_index) / 2);
var o_id=instance_create_layer(x+300, y, "Instances", obj_Door);
physics_fixture_bind(t_fix, id);
physics_fixture_bind(t_fix, o_id);
perma_joint = physics_joint_revolute_create(id, o_id, x+25, y, -90, 90, 1, 10, 2, 0, 0);
physics_joint_enable(perma_joint, 1);
physics_fixture_delete(t_fix);
```

The above code creates and defines a new fixture and then creates an
instance of "obj_Door", binding the created fixture to the two
instances. They are then joined by a revolute joint with no motor and
the angles limited to a +/- 90 degree swing, and we store the joint
index in the variable "perma_joint". We then switch the motor on using
this variable, before finally deleting the fixture from memory as it is
no longer needed.
