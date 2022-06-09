# timeline_exists

With this function you can check and see whether a time line exists
(returns true ) or not (returns false ). This is particularly useful
when creating Timelines dynamically using the [ timeline_add()
](timeline_add) function, but you should note that if you search for
an uninitialised variable (that would otherwise be assigned to a time
line's index) an error will be thrown.

#### Syntax:

``` gml
timeline_exists(ind);
```

|          |                                                                    |                                          |
|----------|--------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                               | Description                              |
| ind      |  [Timeline Asset](../../../../../The_Asset_Editors/Timelines)  | The index of the time line to check for. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if timeline_exists(global.tl)
{
    timeline_delete(global.tl);
}
```

The above code checks to see if a time line exists and is indexed in the
global variable "tl" and if so it then deletes that time line.
