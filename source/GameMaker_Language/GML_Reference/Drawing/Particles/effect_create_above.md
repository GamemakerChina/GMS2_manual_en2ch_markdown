# effect_create_above

With this function you can create a simple effect above all instances of
your room (it is actually created at a depth of -100000). If the effect
is anything other ef_rain or ef_snow then you can define an x/y position
to create the effect, and the size can be a value of 0, 1, or 2, where 0
is small, 1 is medium and 2 is large. It is worth noting that these
effects can have their drawing toggled on and off, as well as have their
drawing paused, by using the functions [ part_system_automatic_draw()
](Particle_Systems/part_system_automatic_draw) and [
part_system_automatic_update()
](Particle_Systems/part_system_automatic_update) with the
appropriate value for the particle system index (where 0 is for effects
below and 1 is for effects above). The available constants for the
different particle kinds are:

<table>
<tbody>
<tr class="header">
<th><span> <a
href="../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/effect_create_above">Effect
Type Constant</a> </span></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th>Constant</th>
<th>Example</th>
<th>Description</th>
</tr>

<tr class="odd">
<td><span> ef_cloud </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/ef_cloud.png" /><br />
</td>
<td>An effect that creates random cloud particles of varying sizes</td>
</tr>
<tr class="even">
<td><span> ef_ellipse </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/ef_ellipse.png" /><br />
</td>
<td>An effect that creates expanding ellipses</td>
</tr>
<tr class="odd">
<td><span> ef_explosion </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/ef_explosion.png" /><br />
</td>
<td>An effect that creates expanding fading explosions</td>
</tr>
<tr class="even">
<td><span> ef_firework </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/ef_firework.png" /><br />
</td>
<td>An effect that creates multiple small particles to generate a
firework explosion</td>
</tr>
<tr class="odd">
<td><span> ef_flare </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/ef_flare.png" /><br />
</td>
<td>An effect that generates a brilliant point that flares up and fades
out</td>
</tr>
<tr class="even">
<td><span> ef_rain </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/ef_rain.png" /><br />
</td>
<td>An effect that generates rain particles coming down from the top of
the screen</td>
</tr>
<tr class="odd">
<td><span> ef_ring </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/ef_ring.png" /><br />
</td>
<td>An effect that generates expanding and fading circles</td>
</tr>
<tr class="even">
<td><span> ef_smoke </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/ef_smoke.png" /><br />
</td>
<td>An effect that generates little puffs of smoke</td>
</tr>
<tr class="odd">
<td><span> ef_smokeup </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/ef_smokeup.png" /><br />
</td>
<td>An effect that creates a smoke plume that rises up the screen</td>
</tr>
<tr class="even">
<td><span> ef_snow </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/ef_snow.png" /><br />
</td>
<td>An effect that generates multiple snow particles falling down the
screen</td>
</tr>
<tr class="odd">
<td><span> ef_spark </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/ef_spark.png" /><br />
</td>
<td>An effect that generates a small spark</td>
</tr>
<tr class="even">
<td><span> ef_star </span></td>
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/ef_star.png" /><br />
</td>
<td>An effect that generates star particles</td>
</tr>
</tbody>
</table>

#### Syntax:

``` gml
effect_create_above(kind, x, y, size, colour);
```

|          |                                                                                                                     |                                                                |
|----------|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Argument | Type                                                                                                                | Description                                                    |
| kind     |  [Effect Type Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/effect_create_above)  | The kind of effect (use one of the constants listed above ).   |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                              | The x positioning of the effect if relevant.                   |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                              | The y positioning of the effect if relevant.                   |
| size     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                              | The size of the effect.                                        |
| colour   |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)            | The colour of the effect.                                      |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if health &amp;lt;= 0
{
    effect_create_above(ef_explosion, x, y, 1, c_yellow);
    instance_destroy();
}
```

The above code will create a medium, yellow, explosion above the
instance and destroy it should the "health" variable be less than or
equal to 0.
