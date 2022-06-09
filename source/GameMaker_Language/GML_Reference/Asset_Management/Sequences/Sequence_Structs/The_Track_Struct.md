# The Track Struct

The track struct can be used either for top-level asset track s or for
sub-track parameter tracks , and the behaviour of the track is defined
by two things, its **name** and its **type** . Track
[structs](../../../../GML_Overview/Structs) are created using the
function [ sequence_track_new() ](../sequence_track_new) and can be
retrieved from sequence assets using the activeTracks property from the
[Sequence Instance Struct](The_Sequence_Instance_Struct) or the
tracks property from the [Sequence Object
Struct](The_Sequence_Object_Struct) . The properties available in
the track struct are:

|                                                                                                                                                |                                                                                                                                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  [Sequence Track Struct](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sequences/Sequence_Structs/The_Track_Struct)  |                                                                                                                                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Variable                                                                                                                                       | Type                                                                                                                                                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|  type                                                                                                                                          |  [Sequence Track Type Constant](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sequences/Sequence_Structs/The_Track_Struct#type)                                                                         | This contains a [Sequence Track Type Constant](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sequences/Sequence_Structs/The_Track_Struct#type) that describes the type of track this is. This can be any one of the constants given under the "Type" section below.                                                                                                                                                                                                                                                    |
|  name                                                                                                                                          |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                                       | When creating a "top-level" asset track, the name you give here can be any string that you require to identify the track. However, for parameter tracks, you need to specify specific strings to tell GameMaker what kind of parameter track you are creating. This is expanded upon under the "Name" section below.                                                                                                                                                                                                                             |
|  tracks                                                                                                                                        |  [Array](../../../../../../GameMaker_Language/GML_Overview/Arrays) of [Sequence Track Struct](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sequences/Sequence_Structs/The_Track_Struct) s          | This property allows access to the list of tracks which are children of this track. When getting this property an [array](../../../../GML_Overview/Arrays) of [Sequence Track Struct](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sequences/Sequence_Structs/The_Track_Struct) s is returned, and when setting this property an array of [Sequence Track Struct](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sequences/Sequence_Structs/The_Track_Struct) s should be specified.     |
|  visible                                                                                                                                       |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                                      | This indicates whether this track is visible (the value is true ) or not (the value is false ). You can get or set this value and if a track not visible then none of its child tracks will be drawn either.                                                                                                                                                                                                                                                                                                                                     |
|  keyframes                                                                                                                                     |  [Array](../../../../../../GameMaker_Language/GML_Overview/Arrays) of [Sequence Keyframe Struct](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sequences/Sequence_Structs/The_Keyframe_Struct) s    | This property allows access to the list of [keyframe structs](The_Keyframe_Struct) for the track. When getting this property an array of keyframe structs is returned, and when setting this property an array of keyframe structs should be specified.                                                                                                                                                                                                                                                                                      |

## Type

The type property can be any one of the following constants (these
constants are also used when generating
[keyframes](../sequence_keyframe_new) and [keyframe
data](../sequence_keyframedata_new) ):

|                                                                                                                                                            |                                                                           |       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|-------|
|  [Sequence Track Type Constant](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sequences/Sequence_Structs/The_Track_Struct#type)  |                                                                           |       |
| Constant                                                                                                                                                   | Description                                                               | Value |
|  seqtracktype_graphic                                                                                                                                      | This is a graphics (sprite) asset track.                                  | 1     |
|  seqtracktype_audio                                                                                                                                        | This is an audio asset track.                                             | 2     |
|  seqtracktype_instance                                                                                                                                     | This is an instance asset track.                                          | 14    |
|  seqtracktype_sequence                                                                                                                                     | This is a sequence asset track.                                           | 7     |
|  seqtracktype_clipmask                                                                                                                                     | This is a clip mask group asset track.                                    | 8     |
|  seqtracktype_clipmask_mask                                                                                                                                | This is a clip mask sprite asset track used for generating the clip mask. | 9     |
|  seqtracktype_clipmask_subject                                                                                                                             | This is a clip mask sprite asset track that is being masked.              | 10    |
|  seqtracktype_group                                                                                                                                        | This group folder asset track.                                            | 11    |
|  seqtracktype_colour                                                                                                                                       | This is a colour data parameter track.                                    | 4     |
|  seqtracktype_real                                                                                                                                         | This is a real number parameter track.                                    | 3     |
|  seqtracktype_message                                                                                                                                      | This is a broadcast message track.                                        | 15    |
|  seqtracktype_moment                                                                                                                                       | This is an event/moment track.                                            | 16    |
|  seqtracktype_text                                                                                                                                         | This is a text track.                                                     | 17    |
|  seqtracktype_bool                                                                                                                                         | Not used currently.                                                       | 5     |
|  seqtracktype_string                                                                                                                                       | Not used currently.                                                       | 6     |
|  seqtracktype_spriteframes                                                                                                                                 | Not used currently.                                                       | 13    |
|  seqtracktype_empty                                                                                                                                        | Not used currently.                                                       | 12    |

## Name

The name property can be any of the following strings:

-   " **position** " - when set on a track which is of type
    seqtracktype_real this indicates that the contents of this track
    should be used as positional data.
-   " **scale** " - when set on a track which is of type
    seqtracktype_real this indicates that the contents of this track
    should be used as scaling data.
-   " **rotation** " - when set on a track which is of type
    seqtracktype_real this indicates that the contents of this track
    should be used as rotation data.
-   " **blend_multiply** " or " **image_blend** " - when set on a track
    which is of type seqtracktype_colour this indicates that the
    contents of this track should be used as colour multiplication data.
    The keyframe data for such a track should be an array of four values
    with the format \[A, R, G, B\]. Note that the values for each
    component are expressed as between 0 and 1, where 0 corresponds to
    the HEX value \#00 and 1 corresponds to the HEX value \#FF (0 - 255
    as shown in the colour picker for image blend tracks in the
    Sequences Editor).
-   " **image_speed** " - when set on a track which is of type
    seqtracktype_real this indicates that the contents of this track
    should be used as the image speed value.
-   " **image_index** " - when set on a track which is of type
    seqtracktype_real this indicates that the contents of this track
    should be used as the image index value.
-   " **image_angle** " - when set on a track which is of type
    seqtracktype_real this indicates that the contents of this track
    should be used as the image angle value. ***Text Track parameter
    names** (only used under Text tracks):*
-   " **frameSize** " - when set on a seqtracktype_real track, this
    indicates that the contents of this track should be used as the
    frame size for the text. E ach keyframe for this track should have
    two channels, 0 and 1, where 0 stores the X size and 1 stores the Y
    size of the frame.
-   " **characterSpacing** " - also used with seqtracktype_real tracks,
    used as the character spacing for the text. Each keyframe for this
    track should have a single channel containing the spacing value.
-   " **lineSpacing** " - also used with seqtracktype_real tracks, used
    as the line spacing for the text. Each keyframe for this track
    should have a single channel containing the spacing value.
-   " **paragraphSpacing** " - also used with seqtracktype_real tracks,
    used as the paragraph spacing for the text. Each keyframe for this
    track should have a single channel containing the spacing value.
