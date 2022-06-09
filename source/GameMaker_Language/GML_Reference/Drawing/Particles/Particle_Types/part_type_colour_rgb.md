# part_type_colour_rgb

With this function you can set the mix of red, green and blue colours
for all particles created of the given type. You supply a minimum value
and a maximum value for each of the three components and the particles
created will have a random colour based on the given range of
parameters. All values must be between 0 and 255.

#### Syntax:

``` gml
part_type_colour_rgb(ind, rmin, rmax, gmin, gmax, bmin, bmax p&amp;gt;
```

|          |                                                                                                                                |                                                        |
|----------|--------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| Argument | Type                                                                                                                           | Description                                            |
| ind      |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)  | The index of the particle type to change.              |
| rmin     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The minimum the final colour's red component can be.   |
| rmax     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The maximum the final colour's red component can be.   |
| gmin     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The minimum the final colour's green component can be. |
| gmax     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The maximum the final colour's green component can be. |
| bmin     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The minimum the final colour's blue component can be.  |
| bmax     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The maximum the final colour's blue component can be.  |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_type_rgb(global.Blood_Part, 0, 255, 0, 0, 0, 0);
```

The above code sets each particle emitted of the particle type indexed
in the global variable "Blood_Part" to be only different shades of red.
