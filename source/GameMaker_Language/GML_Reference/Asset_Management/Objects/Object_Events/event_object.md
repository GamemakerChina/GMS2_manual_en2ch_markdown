# event_object

This **read-only** variable returns object index of the instance which
is running the event being checked.

#### Syntax:

``` gml
event_object;
```

#### Returns:

``` gml
 Object Asset
```

#### Example:

``` gml
global.obj = event_object;
```

The above code stores the object index of the instance performing the
event in a global variable.
