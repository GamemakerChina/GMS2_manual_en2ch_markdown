# Opera GX Game Options

The Opera GX Game Options allow you to modify the properties for your
GXC game. The following sections are provided:

## General

  
![](https://gms.magecorn.com/Manual/assets/Images/Settings/Game_Options/Opera_GX_General_Options.png)  
This section has the following options:

-   **GXC GUID** : This is an identifier (ID) that connects your
    GameMaker project to your game on GXC. When this is empty, your game
    is uploaded as a new game on GXC. When this contains a valid GUID,
    the GXC game associated with that GUID is updated on each new
    upload.
-   **Game Name** : This is your game's name (title) on GXC. You can
    only change this field before your game has been uploaded to GXC
    (when the GUID field is empty). After your first upload, you can
    change your game's name only on GXC.
-   **Version** : This is the version of the game that was last
    uploaded. You can only change this field before your game has been
    uploaded to GXC.
-   **Next Version:** This is the version number used for your next GXC
    upload. You can only change this after your game has been uploaded
    to GXC. You do not need to modify this manually for each upload, as
    GameMaker will automatically increment the last digit of the version
    number for you.
-   **Sign-in and synchronize** : Click on this button to fetch
    information from the GXC game associated with the given GUID. If the
    GUID is invalid, you cannot synchronize.
-   **Team Name** : This is automatically fetched from GXC when your
    project is synchronized. You cannot change this here.
-   **Edit Game on Opera** : This opens GXC DevCloud and takes you to
    your game's "Game details" page. This is only clickable when your
    project is synchronized.
-   **Internal Share URL** : This opens the private version of your
    game, only when it has been enabled on GXC DevCloud.
-   **Public Share URL** : This opens the public version of your game,
    only when it has been enabled on GXC DevCloud. Both of these URLs
    can be shared with others to allow them to play your game.

## Graphics

  
![](https://gms.magecorn.com/Manual/assets/Images/Settings/Game_Options/Opera_GX_Graphics_Options.png)  
Here you can change the following details related to how your game will
be displayed:

-   **Display cursor** : Controls whether the mouse cursor is visible
    when your game starts. Useful for games that don't require mouse
    input or use a [custom mouse
    sprite](../../GameMaker_Language/GML_Reference/General_Game_Control/cursor_sprite)
    .
-   **Interpolate colours between pixels** : Turns on linear
    interpolation , which basically "smooths" pixels. For crisp pixel
    graphics, it should be off, but if you have nice alpha blends and
    smoothed edged graphics it is better left on. This is on by default.
-   **Scaling** : Your game can be configured to scale the draw canvas
    automatically to **maintain the aspect ratio** within the browser,
    or you can select to have it run **full scale** . The full scale
    option will not full screen the game in the browser, but rather
    stretch what is drawn to fit the canvas size, as defined by the
    first room of the game. This is set to keep aspect ratio by default.

Finally there is the option to set the size of the texture page . The
default (and most compatible) size is 2048x2048, but you can choose from
anywhere between 256x256 up to 8192x8192. There is also a button marked
****Preview**** which will generate the texture pages for this platform
and then open a window so that you can see how they look. This can be
very useful if you wish to see how the texture pages are structured and
to prevent having texture pages larger (or smaller) than necessary. For
more information on texture pages, please see
[here](../Texture_Information/Texture_Pages) .
