# instance_create_depth

With this function you can create a new instance of the specified object
at any given point within the room and at the depth specified. The depth
can be any value, where the lower the depth the "nearer" to the camera
things will be drawn and the higher the depth the further away, so an
instance at depth -200 will be drawn over an instance at depth +300 (for
example). Note that this function will actually create a room layer for
the instance, since all instances *must* be on a layer in the room, but
since this is a *managed* layer (i.e.: not one that you have created
through code or in the room, but one that GameMaker has created
automatically). You cannot access that layer, and the [ layer
](Instance_Variables/layer) instance variable will return -1.
IMPORTANT There is a minimum and maximum layer depth of -16000 to 16000.
Anything placed on a depth outside that range **will not be drawn**
although all events will still run as normal. This function returns the
[ id ](Instance_Variables/id) of the new instance which can then be
stored in a variable and used to access that instance. Note that this
function will also call the [Create
Event](../../../../The_Asset_Editors/Object_Properties/Object_Events)
of the instance being created *before* continuing with the code or
actions for the event that called the function.

## Optional Struct

The last argument, var_struct , is optional and takes a struct
containing additional variables for the new instance. Variables from
this struct are applied to the new instance *before* its Create event
runs, but *after* its [Variable
Definitions](../../../../The_Asset_Editors/Object_Properties/Object_Variables)
are set. This means that the values from that struct are readable in the
Create event of the new instance. See **Example 2** at the bottom.
Values applied to the new instance through this struct can be of any
type, including [method](../../../GML_Overview/Method_Variables)
variables. [Built-in
variables](Instance_Variables/Instance_Variables) can be changed as
well. NOTE Variables from the struct are "shallow-copied" to the new
instance, meaning any arrays, structs, and other resources are copied by
reference and not duplicated.

#### Syntax:

``` gml
instance_create_depth(x, y, depth, obj);
```

|            |                                                                         |                                                                  |
|------------|-------------------------------------------------------------------------|------------------------------------------------------------------|
| Argument   | Type                                                                    | Description                                                      |
| x          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x position the object will be created at                     |
| y          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y position the object will be created at                     |
| depth      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The depth to assign the created instance to                      |
| obj        |  [Object Asset](../../../../../The_Asset_Editors/Objects)           | The object index of the object to create an instance of          |
| var_struct |  [Struct](../../../../../GameMaker_Language/GML_Overview/Structs)   |  OPTIONAL A struct with variables to assign to the new instance  |

#### Returns:

``` gml
 Instance ID
```

#### Example 1:

``` gml
var inst = instance_create_depth(x, y, -100, obj_Bullet);
with (inst)
{
    speed = other.shoot_speed;
    direction = other.image_angle;
}
```

The above code creates a new instance of the object obj_bullet at -100
depth, and stores the instance ID in a variable. This variable is then
used to assign speed and direction to the new instance. This will first
create the instance, run its Create event, and *then* assign values to
its variables. If you want to assign some variables *before* the Create
event runs, see the example below.

#### Example 2:

``` gml
var inst = instance_create_depth(x, y, -100, obj_bullet,
{
    speed : shoot_speed,
    direction : image_angle
});
```

The above code creates an instance of obj_bullet , and passes in a
struct as the last argument. That struct has variables for the speed and
direction. It pulls its values from the calling instance, without the
need to use other . These variables are applied to the new instance
before its Create event runs. You're not limited to a struct literal, as
you can also pass in a variable that stores an existing struct, or
create a [new](../../../GML_Overview/Language_Features/new) struct
from a [constructor](../../../GML_Overview/Structs#constr) .
