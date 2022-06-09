# physics_joint_weld_create

The weld joint is designed to attach two fixtures together in a strong,
yet flexible bond. The weld joint will permit flexing between the two
joined fixtures but without the stretching associated with, for example,
a distance joint, and will always try to "spring" back to the reference
angle when put under any stress or load. You define the point in the
room where the joint should be created, as well as the angle that you
wish the joint to try and maintain at all times, as shown in the image
below:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Physics/weld_joint_image.png)  
As you can see, the anchor points are specified as room coordinates so
care must be taken when defining them, especially if the instances are
being created at the same time as the joints rather than being placed in
the room through the room editor. You should also realise that the
joints are created independently of the size of the sprite of the
instances or the fixtures they have attached. So, if you create a weld
joint somewhere other than the origin of the instance, it is still valid
and will constrain the two instances relative to the position at which
it was created. Since the weld joint is flexible and will bend and flex
when under any stress, you can set the oscillation frequency (in Hz) as
well as the damping ratio for the joint to get different effects - you
may need to play with these values to fine tune them and it is
recommended that you start off with smaller values and increment them
until you get the effect that you desire. If you set the "col" value to
true then the two instances can interact and collide with each other but
*only* if they have collision events, however if it is set to false ,
they will not collide no matter what.

#### Syntax:

``` gml
physics_joint_weld_create(inst1, inst2, anchor_x, anchor_y, ref_angle, freq_hz, damping_ratio, col)
```

|               |                                                                                                                       |                                                             |
|---------------|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Argument      | Type                                                                                                                  | Description                                                 |
| inst1         |  [Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)  | The first instance to connect with the joint                |
| inst2         |  [Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)  | The second instance to connect with the joint               |
| anchor_x      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                | The x coordinate for the joint, within the game world       |
| anchor_y      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                | The y coordinate for the joint, within the game world       |
| ref_angle     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                | The joint angle to maintain                                 |
| freq_hz       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                | This is the oscillation frequency for the joint, in hertz   |
| damping_ratio |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                | This damping ratio for the joint                            |
| col           |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                             | Whether the two instances can collide (true) or not (false) |

#### Returns:

``` gml
 Physics Joint ID
```

#### Example:

``` gml
var i, fix, o_id, p_id;
p_id = noone;
o_id = noone;
fix = physics_fixture_create();
physics_fixture_set_box_shape(fix, 64, 32);
for (i = 0; i &amp;lt; 5; i++;)
{
    o_id = instance_create_layer(x + (128 * i), y, "Instances", obj_BridgePart);
    physics_fixture_bind(fix, o_id);
    if i &amp;gt; 0 &amp;amp;&amp;amp; i &amp;lt; 4
    {
        physics_joint_weld_create(p_id, o_id, x + (128 * i) - 64, y, 0, 10, 12, true);
    }
    p_id = o_id;
}
physics-fixture_delete(fix);
```

The above code will create a fixture, then use a loop to create a number
of instances, binding the fixture to each new instance and then joining
them all together using a weld joint. Finally the fixture is deleted
from memory.
