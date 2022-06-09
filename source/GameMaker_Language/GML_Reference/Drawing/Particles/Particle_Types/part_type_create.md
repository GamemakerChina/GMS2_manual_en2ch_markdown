# part_type_create

With this function you can create a new particle type and the return
value should be stored in a variable for use in all subsequent particle
functions.

#### Syntax:

``` gml
part_type_create();
```

#### Returns:

``` gml
 Particle Type ID
```

#### Example:

``` gml
mypart = part_type_create();
```

This will create a new particle type, storing its index in the variable
"mypart".
