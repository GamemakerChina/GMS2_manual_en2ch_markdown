# Cloud Saving

When making games, it is often necessary to store information about the
game state in a file of some type, but storing this information on the
device is not always the best option as, if the player deleted the game
and then re-installs, this information may be lost. To prevent this you
can use various different **cloud services** , which offer data storage
over the internet for retrieval and modification at any time. You should
note that this function is limited to **one** single data "blob" per
game, so every time you send a new save to the cloud service, whether it
is a string or a file, it will overwrite any previously stored data. **
NOTE ** Currently only the **Android** target uses these functions, and
you need to tick the **Enable Google Cloud Saving** checkbox in the
**Social** section of the Android [Game
Options](../../../../Settings/Game_Options/Android) . This will
prompt you to download the [Google
Services](https://marketplace.yoyogames.com/assets/2008/google-play-services)
extension, which is required for cloud saving on Android to function.
For more information on Cloud Saving please see the following helpdesk
article: [Android Cloud
Saving](https://help.yoyogames.com/hc/en-us/articles/360003087452)
GameMaker supports this with a few simple functions that work in
conjunction with the [Asynchronous Cloud
Event](../../../../The_Asset_Editors/Object_Properties/Async_Events/Cloud)
. These functions are explained on the following pages:

-   [cloud_synchronise](cloud_synchronise)
-   [cloud_string_save](cloud_string_save)
-   [cloud_file_save](cloud_file_save)
