# os_lock_orientation

With this function you can "lock" your device to the current orientation
until such time as you "free" it to allow all [Game
Options](../../../Settings/Game_Options) enabled orientations again
for that target platform. Note that you likely want to confirm the
orientation is as desired before locking.

#### Syntax:

``` gml
os_lock_orientation(flag)
```

|          |                                                                         |                                                                    |
|----------|-------------------------------------------------------------------------|--------------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                        |
| flag     |  [Boolean](../../../../GameMaker_Language/GML_Overview/Data_Types)  | Set to true or false to enable or disable orientation locking.     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (os_type == os_android) || (os_type == os_ios)
{
    os_lock_orientation(true);
}
```

The above code checks the OS type and if it is either Android or an iOS
then the orientation locking is flagged as true .
