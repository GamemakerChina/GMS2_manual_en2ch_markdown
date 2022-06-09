# async_load

This variable is **global** in scope and is used to hold a [DS
map](../../../GML_Reference/Data_Structures/DS_Maps/DS_Maps) when
used in the [Asynchronous
Events](../../../../The_Asset_Editors/Object_Properties/Async_Events)
, and -1 at all other times. The actual contents of the DS map will
depend on the type of asynchronous event callback , as well as the
function that was used to trigger the event, so refer to the individual
pages for those events for full details of all the possible DS map
contents.

#### Syntax:

``` gml
async_load;
```

#### Returns:

``` gml
 DS Map ID
```

#### Extended Example:

``` gml
sprite =  sprite_add("site.com/path/image.png", 16, true, true, 0, 0);
```

The above code would be called in an event to load a sprite from an
external URL. This would then trigger the **Image Loaded** Asynchronous
Event, where you would parse the async_load map:

``` gml
if ds_map_find_value(async_load, "id") == sprite
{
    if (ds_map_find_value(async_load, "status") &amp;gt;= 0)
    {
        sprite_index = sprite;
    }
}
```

The above code will first check the ID of the async_load map, then check
the status of the callback. If the value is greater than or equal to 0
(signalling success) the result from the callback will then be used to
set the sprite index of the instance to the newly loaded image.
