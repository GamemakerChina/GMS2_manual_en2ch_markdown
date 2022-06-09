# video_open

This function opens a video file using the path specified. The path can
refer to a file in the [Included
Files](../../../../Settings/Included_Files) of your project, a file
locally present on the user's device, or a URL for loading a file from
the internet (which may not work on all platforms). As you can only load
one video at a time, this function loads the specified video into the
only available "video slot", which is then manipulated via the other
[Video functions](Videos) . There are asynchronous callbacks
associated with video playback. See [Async Callbacks](Videos#h) for
more information.

#### Syntax:

``` gml
video_open(path);
```

|          |                                                                           |                        |
|----------|---------------------------------------------------------------------------|------------------------|
| Argument | Type                                                                      | Description            |
| path     |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Path to the video file |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
my_video = video_open("splash.mp4");
```

The code above loads splash.mp4 from the Included Files of the game.
