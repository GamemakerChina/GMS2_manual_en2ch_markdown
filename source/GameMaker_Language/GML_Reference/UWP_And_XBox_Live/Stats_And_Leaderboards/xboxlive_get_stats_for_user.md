# xboxlive_get_stats_for_user

This function can be used to retrieve data about specific stats from the
Xbox Live servers. You supply the user ID as returned by the function [
xboxlive_get_user() ](../Users_And_Accounts/xboxlive_get_user) ,
then your games Service Configuration ID (as shown on the XDP console),
and finally the stats required. You can request up to a maximum of 14
stats, but this does not guarantee that you will get 14 stat results, as
there is a limit to the total length of the request and therefore the
maximum stat count depends on the length of the names of the stats
themselves. The function will return 0 if the stat request was sent or
-1 if there was an error, and the callback will trigger a [System
Asynchronous
Event](../../../../The_Asset_Editors/Object_Properties/Async_Events/System)
. This event will have the special DS map [ async_load
](../../../GML_Overview/Variables/Builtin_Global_Variables/async_load)
which should then be parsed for the following key:

-   " **event_type** " - should hold the string " **stat_result** " if
    the event was triggered by this function

If the event type relates to this function, then there will also be the
following additional key:

-   " **user** " - holds the user ID for the requested stats.

There may also be an extra set of key value pairs, where the key is the
stat name requested, and the value the value for that stat on the
server. Note that if a stat has never been created for this user
(because they haven't fired the events that set it), no value may be
returned for that stat ( [ ds_map_exists()
](../../Data_Structures/DS_Maps/ds_map_exists) can be used to check
for the stats in the async_load map). If the request fails due to the
request length being to large, there should be a message in the console
output stating the error code:

``` gml
xboxlive_get_stats_for_user - exception occurred getting results - 0x80190190
```

When this happens, the async event DS map should have a "succeeded" key
with a value of "0", and in this case you should attempt to retrieve
fewer stats in a single call.

#### Syntax:

``` gml
xboxlive_get_stats_for_user(user_id, serviceconfig_id, statname1, …);
```

|                          |                                                                                                                              |                                                 |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Argument                 | Type                                                                                                                         | Description                                     |
| user_id                  |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The user ID pointer.                            |
| serviceconfig_id         |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The service config file ID                      |
| statname1 (2, 3, etc...) |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types) s                                                   | The stat names to retrieve the information for. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var _uid = xboxlive_get_user(0);
var _configid = "00000000-0000-0000-0000-000000000000";
xboxlive_get_stats_for_user(xbuser, _configid, "GameProgress", "CurrentMode");
```

The above code gets the user ID and then uses that to request
information about specific stats for that user.
