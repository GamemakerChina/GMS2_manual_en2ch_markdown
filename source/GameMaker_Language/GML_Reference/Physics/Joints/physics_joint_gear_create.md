# physics_joint_gear_create

If you want to create a sophisticated mechanical contraption you might
want to use gears. In principle you can create gears in GameMaker by
using compounding instances to model gear teeth, but this is not very
efficient and might be tedious to author! Thankfully there is a simpler
method, and that is to use a *gear joint* . To make one you need to have
previously defined your fixtures and created the two basic joints that
are going to comprise your gear - these **must** be made up of one
[revolute joint](physics_joint_revolute_create) and either a
[prismatic joint](physics_joint_prismatic_create) or another
*revolute joint* . The image below shows how a gear would typically be
created in a game:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Physics/gear_joint_image.png)  
So what happens? Well, once the two joints are added into the gear,
interaction with one will have an effect on the other, so in the example
image above, if you rotate inst2, inst3 will move up and down, or if you
move inst3 up and down then inst2 will rotate. You can also change the
gear ratio, meaning that you need to move one instance more (or less) to
get the desired effect. The code in the example at the bottom shows how
something like the image above can be created. **NOTE** : If you need to
delete either of the two instances that are involved in the gear joint
(or just delete their joints) then you **must** delete the gear joint
first using [ physics_joint_delete() ](physics_joint_delete) or else
you will get an error!

#### Syntax:

``` gml
physics_joint_gear_create(inst1, inst2, joint_1, joint_2, ratio)
```

|          |                                                                                                                       |                                                    |
|----------|-----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| Argument | Type                                                                                                                  | Description                                        |
| inst1    |  [Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)  | The first instance to connect with the joint       |
| inst2    |  [Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)  | The second instance to connect with the joint      |
| joint_1  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                | A previously defined revolute joint                |
| joint_2  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                | A previously defined revolute *or* prismatic joint |
| ratio    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                | Set the velocity ratio between the two joints      |

#### Returns:

``` gml
 Physics Joint ID
```

#### Example:

``` gml
var t_fix, g_fix, inst1, inst2, inst3, r_joint, p_joint;
g_fix = physics_fixture_create();
physics_fixture_set_box_shape(g_fix, 40, 10);
t_fix = physics_fixture_create();
physics_fixture_set_circle_shape(t_fix, 10);
physics_fixture_set_density(t_fix, 0.5);
inst1 = instance_create_layer(60, room_height - 30, "Background", obj_Ground);
inst2 = instance_create_layer(40, room_height - 300, "Instances", obj_Cog);
inst3 = instance_create_layer(150, room_height - 300, "Instances", obj_Barrel);
physics_fixture_bind(g_fix, inst1);
physics_fixture_bind(t_fix, inst2);
physics_fixture_bind(t_fix, inst3);
r_joint = physics_revolute_joint_create(inst1, inst2, 40, room_height - 300, -80, 80, 1, 10, 0.5, 1, 0);
p_joint = physics_prismatic_joint_create(inst1, inst3, 150, room_height - 300, 0, 1, -10, 10, true, 0, 0, 0, 0);
physics_gear_joint_create(inst2, inst3, r_joint, p_joint, 0.5);
```

The above code creates and defines two fixture and then creates three
instances, one "obj_Ground" and two others, "obj_Cog" and "obj_Barrel".
The fixtures are then bound to these instances and two joints are
created. A revolute joint between the ground and the cog, and a
prismatic joint between the ground and the barrel. Finally a gear joint
is created between the cog and barrel instances using the previously
defined revolute and prismatic joints.
