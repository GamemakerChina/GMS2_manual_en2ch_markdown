# timeline_add

With this function you can add a new (empty) timeline asset into your
game. the function returns the index of this new time line which should
be stored in a variable for use in all further function calls that
involve this new time line. You should also be sure to use the function
[ timeline_delete() ](timeline_delete) whenever you no longer wish
to use the time line (like at the end of the room) so as to prevent any
possible memory leaks that could slow down or crash your game. To add
moments to a timeline created in this way, see the function
[timeline_moment_add_script()](timeline_moment_add_script) .

#### Syntax:

``` gml
timeline_add();
```

#### Returns:

``` gml
 Timeline Asset
```

#### Example:

``` gml
global.tl = timeline_add();
```

The above code creates a new time line and stores its index in the
variable "global.tl".
