# timeline_index

This variable holds the index of the timeline currently associated with
the instance. You can set this to a particular time line to use that
one, or set it to -1 to stop using a time line for the instance (if no
time line is defined for the instance, -1 is returned too). Note that
this does *not* start the time line - for that use the variable [
timeline_running ](timeline_running) .

#### Syntax:

``` gml
timeline_index;
```

#### Returns:

``` gml
 Timeline Asset
```

#### Example:

``` gml
if timeline_exists(global.tl)
{
    timeline_index = global.tl;
}
```

The above code will assign the instance running the code a time line
indexed in the variable "global.tl" if that time line exists.
