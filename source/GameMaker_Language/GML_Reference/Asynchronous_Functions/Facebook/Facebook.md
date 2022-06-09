# Facebook

Facebook is one of the most important social media sites on the internet
and many games and developers currently have their own pages for posting
games and media. GameMaker has an extension that permits you to connect
with Facebook and perform certain actions and tasks that their API
permits. It is recommended that you visit the [Facebook
Developers](https://developers.facebook.com/) page before starting to
use the extension as a firm understanding of how the Facebook Graph
works and the available calls and permissions is essential for you to
get the most from these functions. You can find out how to setup and use
the Facebook extension for all available platforms from the following
link:

-   [Android, iOS and HTML5: Integrating
    Facebook](https://help.yoyogames.com/hc/en-us/articles/360004488072-iOS-Android-and-HTML5-Integrating-Facebook)

The following are **obsolete functions** that were only valid for the
legacy Facebook API. As such you **can no longer use these functions**
in your projects and they are listed here in case you have imported an
old project with them in it. For current Facebook functionality you need
to have activated the **Facebook API** in the appropriate [Game
Options](../../../../Settings/Game_Options) for the target platform,
which will prompt you to download and install an extension. The
extension comes with a \*.pdf format "mini-manual" explaining how to use
it as well as showing all the function definitions and examples. All
references to the old facebook\_\*() functions will need to be replaced
(and updated) to use the extension fb\_\*() equivalents. The functions
listed below were for integrating your game with Facebook:

-    facebook_init
-    facebook_login
-    facebook_request_publish_permissions
-    facebook_request_read_permissions
-    facebook_check_permission
-    facebook_status
-    facebook_accesstoken
-    facebook_user_id
-    facebook_graph_request
-    facebook_dialog
-    facebook_send_invite
-    facebook_post_message
-    facebook_logout
-    facebook_launch_offerwall
