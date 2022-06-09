# Users And Accounts

This section is for users targeting the UWP or Xbox One platforms and
outlines the XBox Live functions available for dealing with users and
user accounts. The Xbox One allows multiple users to sign in to a
console simultaneously. Each user has a specific controller associated
with them and any save game data is also user-specific. To make the most
of this system, GameMaker introduces a number of XBox One only functions
related to the association between controllers and users, permitting you
to query information about the user and also controlling how save data
is handled on a per-user basis. You can find further developer
information about this system from the official white paper on the
[Microsoft developer
site](https://developer.xboxlive.com/en-us/platform/development/education/Documents/Users,%20Controllers,%20and%20Pairing%20-%20Identity%20on%20Xbox%20One.aspx)
. **NOTE** : Note that the User ID is unique to each individual and is
perpetuated across different consoles, so if the same user signs in on
two different devices this User ID will be the same. The following
functions exist for you to use with XBox Live accounts, both on the XBox
One and with the regular UWP export (note this is the minimum
functionality permitted for UWP under the **Creators Program** , as
outlined in [this helpdesk
article](https://help.yoyogames.com/hc/en-us/articles/115002091531-Adding-Xbox-Live-Support-To-Your-UWP-Projects)
):

-   [x](xboxlive_user_is_signed_in)
    [boxlive_user_is_signed_in](xboxlive_user_is_signed_in)
-   [xboxlive_user_is_signing_in](xboxlive_user_is_signing_in)
-   [xboxlive_gamertag_for_user](xboxlive_gamertag_for_user)
-   [xboxlive_show_account_picker](xboxlive_show_account_picker)

The following functions are *only* valid when targeting the XBox One
using UWP with a valid [ID@XBox
account](https://www.xbox.com/es-ES/developers/id) :

-   [xboxlive_get_user_count](xboxlive_get_user_count)
-   [xboxlive_get_user](xboxlive_get_user)
-   [xboxlive_get_activating_user](xboxlive_get_activating_user)
-   [xboxlive_user_is_guest](xboxlive_user_is_guest)
-   [xboxlive_user_is_active](xboxlive_user_is_active)
-   [xboxlive_user_is_remote](xboxlive_user_is_remote)
-   [xboxlive_user_id_for_user](xboxlive_user_id_for_user)
-   [xboxlive_sponsor_for_user](xboxlive_sponsor_for_user)
-   [xboxlive_set_rich_presence](xboxlive_set_rich_presence)
-   [xboxlive_gamedisplayname_for_user](xboxlive_gamedisplayname_for_user)
-   [xboxlive_user_for_pad](xboxlive_user_for_pad)
-   [xboxlive_pad_for_user](xboxlive_pad_for_user)
-   [xboxlive_pad_count_for_user](xboxlive_pad_count_for_user)
-   [xboxlive_agegroup_for_user](xboxlive_agegroup_for_user)
-   [xboxlive_gamerscore_for_user](xboxlive_gamerscore_for_user)
-   [xboxlive_show_profile_card_for_user](xboxlive_show_profile_card_for_user)
-   [xboxlive_reputation_for_user](xboxlive_reputation_for_user)
-   [xboxlive_sprite_add_from_gamerpicture](xboxlive_sprite_add_from_gamerpicture)
-   [xboxlive_generate_player_session_id](xboxlive_generate_player_session_id)
