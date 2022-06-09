# score

This variable is **global** in scope and is used to hold a numeric value
which is usually used for the player score. This variable is only
designed to support legacy projects from previous versions of
*GameMaker* and should ***not be used in new projects*** as it may be
deprecated in the future.

#### Syntax:

``` gml
score;
```

#### Returns:

``` gml
 Real

(single precision floating point value)
```

#### Example

``` gml
switch (object_index)
{
    case obj_Enemy_Fighter:
        score += 10;
    break;

    case obj_Enemy_Mage:
        score += 25;
    break;

    case obj_Enemy_Boss:
        score += 100;
    break;
}
instance_destroy();
```

The above code checks the object index of the instance running the code
using a [switch](../../Language_Features/switch) , and then adds
different amounts to the score variable depending on what object it is.
