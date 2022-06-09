# timeline_get_name

This function can be used to get the name of a time line as a string. if
the time line has been created dynamically using the [ timeline_add()
](timeline_add) function, the name returned will have the format
"\_\_newtimeline *N* " where " *N* " is the number of the time line
(starting from 0). Please note that this is *only* a string and cannot
be used to reference the timeline directly - for that you would need the
*timeline index* . You can, however, use this string to get the
*timeline index* using the returned string along with the function [
asset_get_index() ](../Assets_And_Tags/asset_get_index) .

#### Syntax:

``` gml
timeline_get_name(ind);
```

|          |                                                                    |                                                  |
|----------|--------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                               | Description                                      |
| ind      |  [Timeline Asset](../../../../../The_Asset_Editors/Timelines)  | The index of the time line to check the name of. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var _str = timeline_get_name(timeline_index); show_debug_message("Current timeline = " + _str);
```

The above code get the name of the currently assigned timeline and
output it to the console.
