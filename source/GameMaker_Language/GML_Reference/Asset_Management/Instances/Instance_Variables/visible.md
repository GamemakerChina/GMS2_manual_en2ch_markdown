# visible

An instance can be flagged as visible or not by setting this variable to
true (visible) or false (invisible). This works by telling GameMaker to
skip the draw event for this instance, so care must be taken when using
this as it means that no code placed in the draw event will be run while
the instance is not visible. Also note that if the [layer](layer)
that the instance is assigned to is flagged as invisible, setting this
variable to true will have no effect until the layer itself is flagged
as visible too.

#### Syntax:

``` gml
visible;
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if other.visible = true
{
    x = xprevious;
    y = yprevious;
}
```

The above code will check the visible flag of the "other" instance in a
*collision event* and if it is set to true move that instance back to
its previous position.
