# Path Preferences

  
![](https://gms.magecorn.com/Manual/assets/Images/Setup_And_Version/Preferences/General_Paths_Prefs.png)  
The **Path** preferences control the different file paths required by
elements in the GameMaker IDE as well as for any external editors that
you require. The following options exist for the IDE:

-   **Temp directory** : The location for saving all the temporary
    folders. By default on Windows this is

    ``` gml
    \Users\&amp;lt;Username&amp;gt;\AppData\Local\Temp\GameMaker
    ```

    And on macOS it's:

    ``` gml
    /var/folders/&amp;lt;Path_Hash&amp;gt;/GameMaker
    ```

-   **IDE cache directory** : The location for saving the IDE cache. By
    default on Windows this is

    ``` gml
    \Users\&amp;lt;Username&amp;gt;\AppData\Roaming\GameMaker\Cache
    ```

    And on macOS it's:

    ``` gml
    /Users/&amp;lt;Username&amp;gt;/.config/GameMaker/Cache
    ```

-   **Asset cache directory** : The location for saving the asset cache
    for each project. By default on Windows this is

    ``` gml
    \Users\&amp;lt;Username&amp;gt;\AppData\Roaming\GameMaker\Cache
    ```

    And on macOS it's:

    ``` gml
    /Users/&amp;lt;Username&amp;gt;/.config/GameMaker/Cache
    ```

-   **"My Projects" Location** : The location where GameMaker will
    initially create new projects. By default on Windows this is

    ``` gml
    \Users\&amp;lt;Username&amp;gt;\Documents\GameMaker
    ```

    And on macOS it's

    ``` gml
    /Users/&amp;lt;Username&amp;gt;/GameMaker
    ```

-   **Automatically delete temp directory on close** : Checking this
    will force GameMaker to automatically delete the Temp folder that it
    creates per project for compiling etc... This setting is on by
    default, and un-checking it will switch it off (meaning that you
    will have to manually remove any temp files later).

-   **Automatically delete asset cache on close** : If this is checked
    then the asset compiler cache folder will be removed when you quit
    GameMaker . This is off by default, and enabling it will mean that
    every time you load and run any project the cache will need to be
    rebuilt (which can take time depending on the size of the game).

-   **Automatically delete IDE cache on close** : If this is checked
    then the IDE compiler cache folder will be removed when you quit
    GameMaker . This is off by default, and enabling it will mean that
    every time you start GameMaker the cache will need to be rebuilt.

-   **Delete Temp Folder** : Clicking this button will delete the temp
    folder for the project.

-   **Delete Asset Cache** : Clicking this button will delete the
    compiler asset cache for the project.

-   **Delete IDE Cache** : Clicking this button will delete the IDE
    cache

The following options exist for setting paths to external editors:

-   **Path to external editor/viewer for SWF files** : If you are
    working with SWF format sprites, you can set this to the path of
    your preferred viewer/editor and when you click the *Edit Image*
    button in the Sprite Editor then it will open the given program. The
    default value here is to have no path.
-   **Path to external editor/viewer for Spine files** : If you are
    working with Spine format sprites, you can set this to the path of
    your preferred viewer/editor and when you click the *Edit Image*
    button in the Sprite Editor then it will open the given program. The
    default value here is to have no path.
