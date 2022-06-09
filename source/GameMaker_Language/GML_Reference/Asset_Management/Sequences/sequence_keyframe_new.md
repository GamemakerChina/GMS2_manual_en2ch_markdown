# sequence_keyframe_new

With this function you can create a new track keyframe
[struct](../../../GML_Overview/Structs) , supplying the type of
track that the keyframe will be applied to. The type argument can be any
one of the [Sequence Track Type
Constant](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sequences/Sequence_Structs/The_Track_Struct#type)
s [listed on this page](Sequence_Structs/The_Track_Struct) . The
function will return a [track keyframe
struct](Sequence_Structs/The_Keyframe_Struct) which can then have
data added to it before being assigned to a [track
struct](Sequence_Structs/The_Track_Struct) .

#### Syntax:

``` gml
sequence_keyframe_new(type);
```

|          |                                                                                                                                                         |                                 |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                                                                                                    | Description                     |
| type     |  [Sequence Track Type Constant](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sequences/Sequence_Structs/The_Track_Struct#type)  | The type of keyframe to create. |

#### Returns:

``` gml
 Sequence Keyframe Struct
```

#### Example:

``` gml
myseq = sequence_create();
var mytracks = array_create(1);
mytracks[0] = sequence_track_new(seqtracktype_graphic);
var graphickeys = array_create(1);
graphickeys[0] = sequence_keyframe_new(seqtracktype_graphic);
graphickeys[0].frame = 0;
graphickeys[0].length = 1;
graphickeys[0].stretch = true;
graphickeys[0].disabled = false;
var graphickeydata = array_create(1);
graphickeydata[0] = sequence_keyframedata_new(seqtracktype_graphic);
graphickeydata[0].spriteIndex = spr_Platform;
graphickeydata[0].channel = 0;
graphickeys[0].channels = graphickeydata;
mytracks[0].name = "TestGraphicTrack";
mytracks[0].keyframes = graphickeys;
myseq.tracks = mytracks;
```

The above code creates a new sequence and then creates a graphic asset
track and sets some keyframe data on the track. This track is then
assigned to the instance.
