# timeline_max_moment

This function will return the value of the moment in which the timeline
performs its final action. So, if you have a timeline with 8 different
actions placed 20 moments apart, this function would return the moment
value of the last action in that timeline, which would be 160. This
function is a good way to test whether a timeline has passed the last
active moment when running, since the timeline position will continue
incrementing every step of the game whether there are further actions or
not.

#### Syntax:

``` gml
timeline_max_moment(ind);
```

|          |                                                                    |                                                      |
|----------|--------------------------------------------------------------------|------------------------------------------------------|
| Argument | Type                                                               | Description                                          |
| ind      |  [Timeline Asset](../../../../../The_Asset_Editors/Timelines)  | The index of the timeline to get the last moment of. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if timeline_position &amp;gt; timeline_max_moment(timeline_index)
{
    timeline_running = false;
}
```

The above code will check the current timeline position against the
maximum active moment, and if it is greater the timeline will be
stopped.
