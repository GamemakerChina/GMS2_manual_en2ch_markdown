# gamepad_is_supported

With this function you can find out whether the target platform supports
game pads (returns true ) or not (returns false ).

#### Syntax:

``` gml
gamepad_is_supported();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
global.GP = gamepad_is_supported();
```

The above code checks to see if a gamepad is supported and stores the
return value in a global variable for future checks.
