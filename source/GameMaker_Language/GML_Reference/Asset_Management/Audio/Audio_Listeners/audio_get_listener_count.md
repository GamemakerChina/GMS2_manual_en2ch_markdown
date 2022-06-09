# audio_get_listener_count

Certain target platforms permit more than one listener, so it is
important that you know how many the target has before changing or using
different listeners. This function will return the number of listeners
available.

#### Syntax:

``` gml
audio_get_listener_count();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
global.listener_num = audio_get_listener_count();
```

The above code gets the number of available listeners and stores the
return value in a global variable.
