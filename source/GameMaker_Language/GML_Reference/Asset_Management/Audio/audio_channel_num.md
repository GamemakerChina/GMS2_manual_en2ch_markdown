# audio_channel_num

With this function you can set how many audio channels are available for
playing audio in GameMaker . What this basically means is that you give
the number of simultaneous sounds that can be played at any one time,
and if the number exceeds the amount, those sounds with a lower
*priority* are stopped to free up a channel for the sounds with a higher
*priority* . You can use this function to optimise your game for devices
as the lower the number of channels for audio the better the
performance, but bear in mind that this may also cause noticeable cut
off of certain sounds if many are played at once.

#### Syntax:

``` gml
audio_channel_num(num);
```

|          |                                                                         |                                                      |
|----------|-------------------------------------------------------------------------|------------------------------------------------------|
| Argument | Type                                                                    | Description                                          |
| num      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Number of available audio channels (default is 128). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
switch (os_browser)
{
    case browser_not_a_browser:
        switch (os_type)
        {
            case os_windows:
            case os_macos:
                audio_channel_num(200);
            break;

            default:
                audio_channel_num(64);
            break;
        }
    break;

    default:
        audio_channel_num(16);
    break;
}
```

The above code checks the platform that the game is running on and
changes the number of available sound channels to increase performance.
