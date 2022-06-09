# object_set_sprite

With this function you can set the sprite index of a specific object.
This means that all instances of this object that are created *after the
sprite_index has been changed* will be created with this new
sprite_index, while instances that are already in the room may not be
affected. Please note that this is not an instance function! You can set
the sprite index of individual instances using the [ sprite_index
](../Sprites/Sprite_Instance_Variables/sprite_index) variable and so
have ten instances all with a different sprite to the object they are
created from, and even if you change the sprite index of the object
using this function, all instances that are currently in the room will
remain as they were, and only instances created after calling the
function will start with the new sprite.

#### Syntax:

``` gml
object_set_sprite( index, spr );
```

|          |                                                                |                                     |
|----------|----------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                           | Description                         |
| index    |  [Object Asset](../../../../../The_Asset_Editors/Objects)  | The index of the object to change.  |
| spr      |  [Sprite Asset](../../../../../The_Asset_Editors/Sprites)  | The sprite to assign to the object. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
switch (room)
{
    case rm_start: object_set_sprite(obj_Player, spr_uniform); break;
    case rm_middle: object_set_sprite(obj_Player, spr_swimsuit); break;
    case rm_end: object_set_sprite(obj_Player, spr_casual); break;
}
instance_create_layer(32, 32, "Instances", obj_Player);
```

The above code will set the object "obj_Player" sprite index to
different values depending on the room that the instance running the
code is currently in. It then creates an instance of "obj_Player".
