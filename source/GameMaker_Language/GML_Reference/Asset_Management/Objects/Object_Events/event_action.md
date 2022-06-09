# event_action  DEPRECATED 

This **read-only** variable returns the index of the action currently
being executed, starting at 0 on previous versions of GameMaker.
However, this is **now an obsolete variable** in GameMaker . It has been
left in for legacy support only, and will **always return 0** as all
actions are concatenated together to improve execution speed.

#### Syntax:

``` gml
event_action;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
num = event_action;
```

The above code stores the current action number in the variable "num".
