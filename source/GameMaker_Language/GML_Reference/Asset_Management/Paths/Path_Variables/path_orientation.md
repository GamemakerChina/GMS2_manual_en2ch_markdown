# path_orientation

This variable holds the current orientation of the path that has been
assigned to the instance when the function
[path_start()](../path_start) was called. When a path is created,
its orientation is the default 0 degrees, but you can set this value to
anything you wish using this. Remember that in GameMaker (unless you are
using physics) the angles are calculated counter-clockwise, so setting
the path orientation to 90° would rotate the path to the *left* .  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Paths/pathrotated.png)  

#### Syntax:

``` gml
path_orientation;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
mypath = path_duplicate(choose(path_1, path_2, path_3, path_4)); path_start(path, 4, path_action_reverse, 0); path_orientation = 90;
```

The above code duplicates a random, pre-made path asset into the
variable "mypath". This new path is then started and rotated 90°.
