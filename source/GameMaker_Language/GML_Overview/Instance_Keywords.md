# Instance Keywords

To make certain things easier in GameMaker , you can use one of several
**instance keywords** in your code (whether GML or GML Visual). These
keywords are used primarily to identify instances - and in some cases
structs - under different situations, and each one is explained in the
text below. Note that all the given keywords are represented by
**negative integer values** internally, so care must be taken when
assigning or checking variable values against or with these keywords, as
you may get unexpected results later as GameMaker interprets the value
you have used as something else. You should also note that using the
integer values directly instead of the keywords in your code is **not
recommended at all** and could cause issues later on. [ self self ](#)

|         |                                                                   |       |
|---------|-------------------------------------------------------------------|-------|
| Keyword | Description                                                       | value |
|  self   | The instance/struct which is executing the current block of code. | -1    |

self can be used to identify the current struct or instance that is in
scope in the current block of code. For example:

``` gml
var val = 100;

with (instance_create_layer(x, y, "Instances", obj_Fire))

{

self.val = val;

}
```

In this example you can see that we have a *local* variable called val
and we want it to set the *instance* variable with the same name in the
newly created object instance. To identify the instance variable
correctly and tell GameMaker to set it in the instance calling the code
block, we use the self keyword. In most cases you can also use the id
built-in instance variable instead of self , but self offers certain
benefits. To start with, it is faster for the compiler to identify the
instance (or struct) using self rather than id , as the id value goes
through the instance lookup table while self does not. Secondly, for
those people making extensions, it is very useful to ensure the correct
scoping of variables, since it is possible that a project which uses an
extension may have a global scope variable or something with the same
name as a variable in the extension. **NOTE** : The self keyword is
**not** a shortcut for the actual ID value of an instance or struct and
should only be used in the context explained above. If you require the
ID **value** for an instance then you need to use self.id , eg:

``` gml
var myID = id;

with (all)

{

if self.id == myID

{

// do something

}

}
```

It is also worth noting that self can also be used within
[structs](Structs) - under very specific circumstances - to
reference member variables for the struct. [ other other ](#)

|         |                                                                                          |       |
|---------|------------------------------------------------------------------------------------------|-------|
| Keyword | Description                                                                              | value |
|  other  | The other instance involved in a collision event, in a with function or in a function.   | -2    |

The special keyword other has multiple ways that it can be used to
reference a specific instance (and in some cases, a struct): it can be
used in a with statement (explained [here](Language_Features/with)
), in a [collision
event](../../The_Asset_Editors/Object_Properties/Object_Events) , or
in a function. This section is going to explain the last two use cases.
Do note that in events other than the collision event, when outside of
any function calls and with() blocks, other simply returns the struct
for the current instance.

## Collision Event

A collision event can only happen between **two** instances. You *can*
have multiple collisions between multiple instances, but they are all
resolved by GameMaker on a 1-on-1 basis, with the "self" instance that
has the collision event and the "other" instance that is colliding with
it. Imagine you have a player instance, multiple enemy instances and
multiple bullet instances that the enemy can fire at you. You can assign
each enemy a single bullet instance but with a different damage variable
randomly assigned to it when created, for example:

``` gml
var bullet;

bullet = instance_create_layer(x, y, "Bullets", obj_Bullet);

bullet.damage = 5 + irandom(5);

bullet.speed = 8;

bullet.direction = point_direction(x, y, obj_Player.x, obj_Player.y);
```

You can see how we set its variables using the dot notation as outlined
in the section on [Addressing Variables In Other
Instances](Addressing_Variables_In_Other_Instances) . This will give
each bullet instance a different damage value, but how will the player
detect the damage that it has to take when it's hit by a bullet? For
this, the player will need to have a collision event with obj_Bullet ,
and within that event use other to read variables from the colliding
bullet instance:

``` gml
hp -= other.damage;

if hp &amp;lt;= 0 instance_destroy();
```

The above code will deduct the amount stored in the *other* instance's
"damage" variable from the player's "hp" variable, then it will check to
see if the "hp" is lower than or equal to 0. If it is then it will
destroy the player instance. Please note that the other instance must
have the variable being checked or else an error will be thrown.
**NOTE** : The Collision event is the only event that has a special
meaning for the other keyword. In all other events and scripts, the
behaviour of other will be defined by the context it is being used in
(such as a with() block, a function, struct declaration, etc.). You can
assign values to variables, or even create new ones, using other in the
collision event, like this:

``` gml
// add ten to the other instance "mana" variable

other.mana += 10;

// set the other instance variable "hit" to true, creating the variable if it doesn't already exist

other.hit = true;
```

## Struct Declaration

When used inside a struct declaration, other refers to the instance that
is initialising the struct:

``` gml
var _struct =

{

parent_instance : other

}


show_debug_message(_struct.parent_instance == self);

// This prints '1' (true) meaning that both sides refer to the same instance
```

However, you do not need to use other to read variables from the
instance as any variables you reference directly will be read from that
instance's scope, as described [in this
section](Structs#inst_in_struct) of the manual. You would only need
to use this if you wanted to store a reference to that instance's
struct.

## Instance Method

Using other within another instance's [method](Method_Variables)
refers to the instance that called that method. For example, let's say
Object2 has a method that references self and other . This method is
then called in Object1 . Since the method was created in Object2 , it is
**bound** to it and will always use the Object2 instance as the "self",
no matter which instance calls it. In such a case, the calling instance
becomes other .

``` gml
// In Object2

my_method = function()

{

show_debug_message(object_get_name(self.object_index));

show_debug_message(object_get_name(other.object_index));

}


// In Object1

Object2.my_method();
```

This would cause the instance to first print its own object
name ("Object2") and then the object name of the calling instance
("Object1"). The same will apply to a method that is bound to a struct.

## Constructor Function

When used within a constructor function, other will reference the
instance that is calling that function, however this is not recommended
for general use as any external data that a constructor needs to use
should be passed in as arguments. [ all all ](#)

|         |                                             |       |
|---------|---------------------------------------------|-------|
| Keyword | Description                                 | value |
|  all    | All instances currently active in the room. | -3    |

This keyword is used to tell GameMaker that a function is to be applied,
or to check, all active instances within a room (deactivated instances
will not be checked or accessed). You **cannot** use all to access or
set variables in other instances using the point method (see
[here](Addressing_Variables_In_Other_Instances) ), but you **can**
use it when calling [ with() ](Language_Features/with) , for
example:

``` gml
with (all)

{

speed = 0;

}
```

The above code will set the speed of all instances in the room to 0. You
can also use all within functions to target or check all instances in
the room for example:

``` gml
// Check a point for any active instance in the room

inst = instance_position(mouse_x, mouse_y, all);


// Check all instances for a collision along a line

if collision_line(x, y, mouse_x, mouse_y, all, false, true) {}


// Add all instances in the room into a motion planning grid

mp_grid_add_instances(grid, all, false);
```

all is a very useful keyword and can be used in numerous situations
within your code and actions, often cutting down on the amount of code
you need to write to achieve a desired effect. [ noone noone ](#)

|         |                     |       |
|---------|---------------------|-------|
| Keyword | Description         | value |
|  noone  | No instance at all. | -4    |

It may seem odd, but many times while programming your games will you
find the need to check if there are no instances found at a location, or
in a collision etc... In those cases you would use this keyword to check
for nothing, something like this:

``` gml
if instance_nearest(x, y, obj_enemy) != noone

{

//do something as there is an enemy instance near

}
```

In this example, the function instance_nearest() will return either
noone or the unique ID of the nearest found instance. Basically, any
time that you need to check for an instance, you can expect to get
either noone or a unique instance ID returned.
