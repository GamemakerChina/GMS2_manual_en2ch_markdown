# Push Notifications

  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Async_Push.png)  
The Push Notification Event is triggered by the callback from [**push
notifications**](../../../GameMaker_Language/GML_Reference/Asynchronous_Functions/Push_Notifications/Push_Notifications)
on the device OS, either from a local source or a remote source. It
generates a [DS
Map](../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/DS_Maps)
that is exclusive to this event and is stored in the special variable [
async_load
](../../../GameMaker_Language/GML_Overview/Variables/Builtin_Global_Variables/async_load)
. This event is exclusively used by extensions (such as the [Firebase
Cloud
Messaging](https://marketplace.yoyogames.com/assets/10451/firebase-cloud-messaging-ext)
extension), so please refer to your extension's documentation for
instructions on using this event.
