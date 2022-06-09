# UWP And Xbox Live

This section outlines the functions specifically for use when targeting
the UWP target platform. The initial set of functions are for
controlling the general game behaviour when creating a UWP app:

-   [uwp_suspend](uwp_suspend)
-   [uwp_is_suspending](uwp_is_suspending)
-   [uwp_is_constrained](uwp_is_constrained)
-   [uwp_was_terminated](uwp_was_terminated)
-   [uwp_was_closed_by_user](uwp_was_closed_by_user)
-   [uwp_show_help](uwp_show_help)
-   [uwp_license_trial_version](uwp_license_trial_version)
-   [uwp_license_trial_user](uwp_license_trial_user)
-   [uwp_license_trial_time_remaining](uwp_license_trial_time_remaining)
-   [uwp_check_privilege](uwp_check_privilege)

UWP also permits you to create games for the XBox One platform using the
XBox Live API using the following functions. These functions require you
to have checked the **Enable XBox Live** option in the [UWP Game
Options](../../../Settings/Game_Options/Windows_UWP) . Some of these
functions require the user to be signed-in to XBox Live, which GameMaker
will try to do automatically when you run the project. This "silent"
sign in will generate a [System Asynchronous
Event](../../../The_Asset_Editors/Object_Properties/Async_Events)
which can the be checked to see if it was successful or not before
proceeding. Note that unlike the Xbox One Console export, the UWP export
for XBox Live only permits one user to be signed-in at a time.
**IMPORTANT!** The UWP target only has a minimum of support for XBox
Live when set up as part of the **Creator Program** , which is limited
to some basic user and account functions (see
[here](https://help.yoyogames.com/hc/en-us/articles/115002091531-Adding-Xbox-Live-Support-To-Your-UWP-Projects)
for more information on setting this up). To be able to use all the
functionality listed here you will need to have an [ID@XBox
account](https://www.xbox.com/es-ES/developers/id) . You can find all
the various XBox Live functions for use with the UWP export target from
the sections listed below:

-   [Users And Accounts](Users_And_Accounts/Users_And_Accounts)
-   [Saving Data](Saving_Data/Saving_Data)
-   [Stats And
    Leaderboards](Stats_And_Leaderboards/Stats_And_Leaderboards)
-   [Match Making](Match_Making/Match_Making)
