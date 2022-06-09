# timeline_clear

With this function you can clear a specific time line of "moments",
removing all codes and actions for that time line and leaving it empty.

#### Syntax:

``` gml
timeline_clear(ind);
```

|          |                                                                    |                                     |
|----------|--------------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                               | Description                         |
| ind      |  [Timeline Asset](../../../../../The_Asset_Editors/Timelines)  | The index of the timeline to clear. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if timeline_position &amp;gt; 200
{
    timeline_clear(global.tl);
    timeline_index = -1;
}
```

The above code will clear the specified time line indexed by the
variable "global.tl" of all moments when a specific moment has been
passed.
