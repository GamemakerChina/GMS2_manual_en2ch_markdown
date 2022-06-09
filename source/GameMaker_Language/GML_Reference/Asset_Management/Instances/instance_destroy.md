# instance_destroy

You call this function whenever you wish to "destroy" an instance,
normally triggering a [Destroy
Event](../../../../The_Asset_Editors/Object_Properties/Object_Events)
and also a [Clean Up
Event](../../../../The_Asset_Editors/Object_Properties/Object_Events)
. This will remove it from the room until the room is restarted (unless
the room is persistent). Calling the function with no arguments will
simply destroy the instance that is currently in scope and running the
code, but you can provide an optional "id" argument and target a
specific instance by using the instance [id](Instance_Variables/id)
value, or you can target all instances of a particular object by using
an [ object_index ](../Objects/object_index) . For example:

``` gml
instance_destroy(other);      // destroy the "other" instance in a Collision Event
instance_destroy(obj_Bullet); // destroy ALL instances of the object "obj_Bullet"
```

The second *optional* flag permits you to "switch off" the Destroy Event
for the instance being destroyed. By default the Destroy Event will
*always* be performed, but if you set this flag to false then you can
make the instance destroy itself and skip performing that event.
**IMPORTANT!** This will skip the Destroy Event, but the Clean Up event
will still be called. It is worth noting that when you destroy an
instance, its destroy event is called *immediately* after the code or
action that calls the destroy function. Also, although the destroy event
is performed, the instance *is not immediately removed from the game* ,
and it will continue to perform the code contained in the current event.
Only when the current event is over will it be removed from the game.
So, if you have, for example, this code:

``` gml
if (hp &amp;lt;= 0) instance_destroy();
score += 10;
```

The variable "score" will be incremented *even though the
instance_destroy function has been called* , and the instance will
finally be removed from your game at the end of the event. Be careful of
this, as if you have (for example) created a dynamic resource for the
instance, like a data structure, and then have destroyed that resource
in the destroy event, if there are any references to it after the
destroy function or action has been performed then you will get an
"unknown resource" error, as the destroy event removed it from the game.

#### Syntax:

``` gml
instance_destroy([id, execute_event_flag]);
```

|                    |                                                                                                                                                                                         |                                                                                                                                |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Argument           | Type                                                                                                                                                                                    | Description                                                                                                                    |
| id                 |  [Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id) or [Object Asset](../../../../../The_Asset_Editors/Objects)    |  OPTIONAL The instance ID to destroy, or the object asset to destroy instances of (optional, default is the calling instance)  |
| execute_event_flag |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                               |  OPTIONAL Set to true or false to perform the Destroy event or not (optional, default is true )                                |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (bbox_right &amp;lt; 0 || bbox_left &amp;gt; room_width || bbox_bottom &amp;lt; 0 || bbox_top &amp;gt; room_height)
{
    instance_destroy(id, false);
}
```

The above code will destroy the instance running the code without
calling the Destroy Event if the instance is outside the room bounds.
