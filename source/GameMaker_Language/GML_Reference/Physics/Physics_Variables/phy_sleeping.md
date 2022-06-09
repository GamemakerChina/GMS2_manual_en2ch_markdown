# phy_sleeping

This **read-only** variable returns whether or not the instance is
currently "sleeping" ( true ) or not ( false ), A "sleeping" instance is
one that is not actively engaged in any physical simulation. GameMaker
will put objects to sleep to save simulation cycles when an instance is
at rest and not in collision with another instance

#### Syntax:

``` gml
phy_sleeping;
```

#### Returns:

``` gml
 Boolean

(or undefined if the instance is not physics enabled)
```

#### Example:

``` gml
if phy_sleeping
{
    instance_destroy();
}
```

The above code checks to see if the object is being actively simulated
or not and if it is not it is destroyed.
