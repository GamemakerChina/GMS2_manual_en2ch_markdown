# In App Purchase

  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Async_IAP.png)  
This event can only be triggered by the various **In App Purchase**
(IAP) extensions for the different target platforms available on the
[Marketplace](../../../Introduction/The_Marketplace) . This event
will always generate a DS map that is exclusive to this event and stored
in the special variable [ async_load
](../../../GameMaker_Language/GML_Overview/Variables/Builtin_Global_Variables/async_load)
. This DS map will have different key/value pairs depending on the
extension function that triggered it, but there will always be an " id "
key which can then be used to identify the type of In App Purchase event
that it is. For exact details of the possible return values and
functions that generate this event, please see the individual PDF
manuals included with each of the extensions.
