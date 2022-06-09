# image_xscale

This value sets the horizontal scaling applied to the sprite that has
been assigned to the current instance. A scale of 1 indicates no scaling
(1:1), smaller values will scale down (0.5, for example, will half the
width of the sprite), larger values will scale up and negative values
will flip the sprite *and* scale it unless the value used is exactly -1
(in which case the sprite is just flipped about its origin with no
scaling).  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Sprites/xscale_image.png)  

#### Syntax:

``` gml
image_xscale;
```

#### Returns:

``` gml
 Real

(single precision floating point value)
```

#### Example:

``` gml
if image_xscale &amp;lt; 5
{
    image_xscale += 0.2;
    image_yscale = image_xscale;
}
else
{
    instance_create_layer(x, y, "Effects", obj_Explosion);
    instance_destroy();
}
```

The above code scales the sprite and then once it is scaled to 5 times
its original size, a new instance of another object is created and the
instance destroyed.
