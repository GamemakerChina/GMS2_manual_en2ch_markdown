# skeleton_skin_get

With skeletal animation sprites, you can assign separate textures
(called "skins") to the animation, thereby using one animation for
multiple different things. This function will return the name of the
skin (as a string) that is currently assigned to the skeletal animation
sprite your instance is using. The name returned is that which you set
when you created the sprite in your animation program.

#### Syntax:

``` gml
skeleton_skin_get();
```

#### Returns:

``` gml
 String
```

#### Example:

``` gml
if skeleton_skin_get() == "skin_Enemy1"
{
    skeleton_skin_set(choose("skin_Enemy1", "skin_Enemy2", "skin_Enemy3");
}
```

The above code would check the currently assigned skin for the animation
and if it is "skin_Enemy1", it chooses and sets a new skin from one of
three options.
