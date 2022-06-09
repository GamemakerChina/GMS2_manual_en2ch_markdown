# gc_get_stats

With this function you can retrieve information about the current state
of the garbage collector. The function will return a
[struct](../../GML_Overview/Structs) which will have the following
member variables (note that "objects" here refers to anything that can
be garbage collected and *not* general object instances as defined in
the Asset Browser):

|                                                                                                       |                                                                                                                                             |                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
|  [GC Stats Struct](../../../../GameMaker_Language/GML_Reference/Garbage_Collection/gc_get_stats)  |                                                                                                                                             |                                                                                                                                                     |
| Variable                                                                                              | Type                                                                                                                                        | Description                                                                                                                                         |
|  objects_touched                                                                                      |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                         | This is the number of active objects the garbage collector found in the previous frame. This will vary depending on which generation was collected. |
|  objects_collected                                                                                    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                         | The number of objects which the garbage collector determined weren't active in the previous frame, and which could therefore be deleted.            |
|  traversal_time                                                                                       |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                         | This is the time in microseconds (on the main thread) which the garbage collector took to figure out which objects were active.                     |
|  collection_time                                                                                      |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                         | This is the time in microseconds (on a separate thread) which the garbage collector took to clean up the objects deemed inactive.                   |
|  gc_frame                                                                                             |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                         | This is a counter which is incremented every time a garbage collection pass occurs. If garbage collection is disabled this will not increase.       |
|  generation_collected                                                                                 |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                         | This is the index of the generation that was collected last. 0 is the youngest generation and 3 is currently the oldest.                            |
|  num_generations                                                                                      |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                         | This is the total number of garbage collection generations.                                                                                         |
|  num_objects_in_generation                                                                            |  [Array](../../../../GameMaker_Language/GML_Overview/Arrays) of [Real](../../../../GameMaker_Language/GML_Overview/Data_Types) s    | This is an array (of size num_generations ) containing the number of objects in each generation.                                                    |

**NOTE** : On the HTML5 target platform garbage collection is handled by
the JavaScript engine and therefore the member variables in the above
struct will all return 0 if this function is used on that platform. When
using this function, please note that the information shown for the
objects *is only updated when a full generation is finished processing*
, which may take several frames depending on frame time setting (see
[here](gc_target_frame_time) for more information on frame timing).

#### Syntax:

``` gml
gc_get_stats();
```

#### Returns:

``` gml
 GC Stats Struct
```

#### Example:

``` gml
if (global.debug == true)
{
    var _s = gc_get_stats();
    var _t = _s.traversal_time;
    var _c = _s.collection_time;
    show_debug_message("Traversal time = " + string(_t))
    show_debug_message("Collection time = " + string(_c))
}
```

The above code checks a global variable and if it is true it gets
information from the garabge collector and outputs it to the console as
debug messages.
