# mask_index

When you define an object in GameMaker you can assign it a mask to be
used for collisions rather than the one that corresponds to the defined
sprite. This variable can be used to find the [ sprite_index
](sprite_index) of that mask (or it will return -1 if no sprite has
been assigned) or to set the mask for an instance to the chosen sprite.
Setting the mask index means that you can have, for example, a sprite
for the instance with an irregular shape, yet give it a circular
collision mask that is gotten from a different sprite.

#### Syntax:

``` gml
mask_index;
```

#### Returns:

``` gml
 Sprite Asset
```

#### Example:

``` gml
mask_index = spr_Round;
```

The above code sets the mask of the instance to that of the sprite
"spr_Round".
