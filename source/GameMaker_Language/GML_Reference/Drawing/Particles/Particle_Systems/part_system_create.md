# part_system_create

This function is used to create a new particle system and will return a
unique index number that should be stored and used in all further
functions relating to that system. The system will be assigned a managed
layer and will be set to have a depth of 0. Managed layers are not
accessible to the user and used only for internal management when depth
is used instead of layers. Normally you would use the function [
part_system_create_layer() ](part_system_create_layer) instead of
this one.

#### Syntax:

``` gml
part_system_create();
```

#### Returns:

``` gml
 Particle System ID
```

#### Example:

``` gml
global.Sname = part_system_create();
```

This will create a new particle system and store the index in the global
variable "Sname".
