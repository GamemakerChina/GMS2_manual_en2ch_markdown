# physics_pause_enable

Normally for a physics simulation to work, it must be continuous and
cannot be stopped and started, or have instances suddenly moved from one
place to another in the room. However, there are moments when you *need*
to pause the simulation as (for example) the device os has paused, and
so you would use this function. It pauses the simulation if the flag is
set to true and no further physics calculations will be done until the
flag is set to false again. **NOTE** : This is of particular use should
you wish to deactivate all the instances in a room as even when
deactivated a physical body will still continue being calculated and
simulated in the physics world.

#### Syntax:

``` gml
physics_pause_enable(flag)
```

|          |                                                                            |                                                                                  |
|----------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                                      |
| flag     |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | This can be set to true to pause the simulation, or false to start it again.     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if os_is_paused()
{
    physics_pause_enable(true);
    instance_deactivate_all(true);
    instance_create_layer(x, y, "Controllers", obj_PauseMenu);
}
```

The code above checks to see if the OS has been paused and if it has
then it pauses the physics world, deactivates everything except itself,
and then creates a pause menu instance.
