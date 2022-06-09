# Particle Action Library

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/Lib_Particles.png)  
For complex things in GameMaker you would normally have an *object* and
then create *instances* of that object within the *room* . However, for
graphics effects, this can be expensive as every instance comes with a
"cost" in processing due to the variables it contains and the codes it
has in the different events. You can reduce this cost by turning to
tiles for drawing your graphics, or even using the *asset layer* in the
room editor, but both of those are generally only used for drawing
simple graphics that maintain the same position over time and have few
special effects. However, there is one other option for drawing fast yet
versatile graphics effects in your games, and that is to use particles.
Particles are graphic resources with certain properties which are
defined within a **particle system** . These properties cannot be
manipulated directly for individual particles, but are changed through
the actions that are used to define the individual **particle types**
within the system. They are very useful for creating beautiful and
flashy effects (or subtle and discreet ones!) like explosions, decals,
rain, snow, star fields and debris in a game without the CPU or GPU
overhead that using instances and/or tiles and assets have. The basic
setup for a particle system follows three steps:

-   **Create a Particle System** : The particle system is like a
    container that we will use to hold our different particle emitters
    as we use them. We use actions to define a series of visual aspects
    and behaviours for our particles, and then we use them from an
    emitter that has been placed in the "container" (the particle
    system) so that they can be seen.
-   **Create Particle Types** : Particle "types" are the definition of
    the graphic effect itself. You can have many different particle
    types, each with their own range of colours, alphas, sizes and
    movements, but its important to note *that you do not have control
    over individual particles* . You define a series of parameters and
    the particle will be created to have a random spread of behaviours
    chosen from them.
-   **Create Particle Emitters** : Emitters are used to burst or stream
    particles from within very clearly defined limits, and can be given
    special parameters to define exactly *how* a given particle effect
    should be created. Emitters can be optional, as you can use the
    action [Burst Particles](Burst_Particles) to emulate many of the
    effects of an emitter, with the added bonus of not needing to worry
    about cleaning up the emitter later. Note, that emitters, unlike
    particles, must belong to a system for any particles being created
    to be seen.

You can get a more in-depth guide to setting up and using particles from
the following page of the manual:

-   [Guide To Using
    Particles](../../../Additional_Information/Guide_To_Using_Particles)

Although particles are an excellent tool for creating effects, they do
come with certain restrictions and rules of good practice which need to
be followed unless you want your game to have issues:

-   The particle system, particle types and particle emitters all take
    up *memory* and as such you should be very careful how you use them
    as it is very easy to cause a memory leak which will slow down and
    eventually crash your game, so each particle type and emitter (and
    possibly the system itself) should be destroyed the moment it is not
    needed.
-   Particles may be fast and light on the CPU and GPU, but they still
    require some processing and so you shouldn't have 40,000 of them
    bursting across the screen at a time. Limit them to those that are
    necessary to achieve a specific effect and no more.
-   If you define your own particle sprite instead of using one of the
    14 included sprites, you should try to keep them as small as
    possible to achieve the effect you require.
-   Particles do *not* interact with anything. Should you need them to
    have any type of interaction with the user or any other instances in
    your game, you should be looking at using instances instead as
    particles are purely graphic.
-   Even though there is no technical limit to the amount of emitters
    and particles you can create in one game, you should try and limit
    everything to the minimum number possible to keep memory use as low
    as possible.
-   On mobile devices, take care with particles as drawing them can be
    slow if they cover a large area of the screen (over-draw on mobile
    devices is one of the main causes of slowdown).
-   When targeting the HTML5 platform, note that unless you have WebGL
    enabled, you cannot have colour blending either (only the first of
    the particle colours will be used on non-WebGL canvas).

The following sections cover all actions for making your own particle
systems:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Create_Particle_System.png" /><br />
</td>
<td><a href="Create_Particle_System">Create Particle System</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Destroy_Particle_System.png" /><br />
</td>
<td><a href="Destroy_Particle_System">Destroy Particle
System</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Clear_Particle_System.png" /><br />
</td>
<td><a href="Clear_Particle_System">Clear Particle System</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Pause_Particle_System.png" /><br />
</td>
<td><a href="Pause_Particle_System">Pause Particle System</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Update_Particle_System.png" /><br />
</td>
<td><a href="Update_Particle_System">Update Particle System</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Create_Particle_Type.png" /><br />
</td>
<td><a href="Create_Particle_Type">Create Particle Type</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Destroy_Particle_Type.png" /><br />
</td>
<td><a href="Destroy_Particle_Type">Destroy Particle Type</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Set_Particle_Size.png" /><br />
</td>
<td><span> </span> <span> </span> <span> </span> <span> </span> <span>
</span> <span> </span> <span> </span> <a
href="Set_Particle_Size">Set Particle Size</a> <span> </span></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Set_Particle_Sprite.png" /><br />
</td>
<td><a href="Set_Particle_Sprite">Set Particle Sprite</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Set_Particle_Shape.png" /><br />
</td>
<td><a href="Set_Particle_Shape">Set Particle Shape</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Set_Particle_Colour.png" /><br />
</td>
<td><a href="Set_Particle_Colour">Set Particle Colour</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Set_Particle_Alpha.png" /><br />
</td>
<td><a href="Set_Particle_Alpha">Set Particle Alpha</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Set_Particle_Life.png" /><br />
</td>
<td><a href="Set_Particle_Life">Set Particle Life</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Set_Particle_Speed.png" /><br />
</td>
<td><a href="Set_Particle_Speed">Set Particle Speed</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Set_Particle_Direction.png" /><br />
</td>
<td><a href="Set_Particle_Direction">Set Particle Direction</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Set_Particle_Orientation.png" /><br />
</td>
<td><a href="Set_Particle_Orientation">Set Particle
Orientation</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Set_Particle_Gravity.png" /><br />
</td>
<td><a href="Set_Particle_Gravity">Set Particle Gravity</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Set_Secondary_Particles.png" /><br />
</td>
<td><a href="Set_Secondary_Particles">Set Secondary
Particles</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Burst_Particles.png" /><br />
</td>
<td><a href="Burst_Particles">Burst Particles</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Create_Particle_Emitter.png" /><br />
</td>
<td><a href="Create_Particle_Emitter">Create Particle
Emitter</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Destroy_Particle_Emitter.png" /><br />
</td>
<td><a href="Destroy_Particle_Emitter">Destroy Particle
Emitter</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Emit_Particles.png" /><br />
</td>
<td><a href="Emit_Particles">Emit Particles</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Set_Emitter_Region.png" /><br />
</td>
<td><a href="Set_Emitter_Region">Set Emitter Region</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Do_Effect.png" /><br />
</td>
<td><a href="Do_Effect">Do Effect</a></td>
</tr>
</tbody>
</table>
