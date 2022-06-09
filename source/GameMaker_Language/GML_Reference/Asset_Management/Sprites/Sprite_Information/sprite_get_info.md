# sprite_get_info

This function is used to retrieve information for the given sprite. You
supply a sprite index (which can be an asset added through the [Asset
Browser](../../../../../Introduction/The_Asset_Browser) or a sprite
[added](../Sprite_Manipulation/sprite_add) at runtime) and the
function returns a [struct](../../../../GML_Overview/Structs) with
the following variables:

|                                                                                                                                            |         |                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  [Sprite Info Struct](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Information/sprite_get_info)  |         |                                                                                                                                                                                                                                          |
| Variable                                                                                                                                   | Type    | Description                                                                                                                                                                                                                              |
| **width**                                                                                                                                  | real    | The sprite's width (in pixels)                                                                                                                                                                                                           |
| **height**                                                                                                                                 | real    | The sprite's height (in pixels)                                                                                                                                                                                                          |
| **xoffset**                                                                                                                                | real    | The sprite's X offset/origin (in pixels)                                                                                                                                                                                                 |
| **yoffset**                                                                                                                                | real    | The sprite's Y offset/origin (in pixels)                                                                                                                                                                                                 |
| **transparent**                                                                                                                            | boolean |  true if the sprite is marked as transparent, otherwise false (This can only be specified through [sprite_add()](../Sprite_Manipulation/sprite_add) or similar functions, and will be false for sprites created in the IDE)          |
| **smooth**                                                                                                                                 | boolean |  true if the sprite is marked as smooth, otherwise false (This can only be specified through [sprite_add()](../Sprite_Manipulation/sprite_add) or similar functions, and will be false for sprites created in the IDE)               |
| **type**                                                                                                                                   | real    | The type of the sprite: 0  - Bitmap (Regular sprites) 1  - SWF 2  - Spine                                                                                                                                                                |
| **bbox_left**                                                                                                                              | real    | Position of the left edge of the bounding box (in pixels)                                                                                                                                                                                |
| **bbox_top**                                                                                                                               | real    | Position of the top edge of the bounding box (in pixels)                                                                                                                                                                                 |
| **bbox_right**                                                                                                                             | real    | Position of the right edge of the bounding box (in pixels)                                                                                                                                                                               |
| **bbox_bottom**                                                                                                                            | real    | Position of the bottom edge of the bounding box (in pixels)                                                                                                                                                                              |
| **name**                                                                                                                                   | string  | The name of the sprite                                                                                                                                                                                                                   |
| **num_subimages**                                                                                                                          | real    | The number of sub-images (or frames) in the sprite                                                                                                                                                                                       |
| **use_mask**                                                                                                                               | boolean |  true if this sprite uses a collision mask, otherwise false                                                                                                                                                                              |
| **num_masks**                                                                                                                              | real    | The number of masks in this sprite (will be greater than 1 if the sprite uses per-frame masks)                                                                                                                                           |
| **nineslice**                                                                                                                              | struct  | The [Nine Slice struct](../Nine_Slice_Struct) for this sprite, or undefined if it has no nine slice data                                                                                                                             |
| **messages**                                                                                                                               | array   | Array of broadcast messages for this sprite, where each broadcast message is a struct containing information on the message (more information under "General Sprite Data")                                                               |
| **frame_info**                                                                                                                             | array   | Array of frames for this sprite, where each frame is a struct containing information on its timing (more information under "General Sprite Data")                                                                                        |

**This additional variable is available only for Bitmap
(regular) sprites:**

|                                                                                                                                            |       |                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------|
|  [Sprite Info Struct](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Information/sprite_get_info)  |       |                                                                                                                                                   |
| Variable                                                                                                                                   | Type  | Description                                                                                                                                       |
| **frames**                                                                                                                                 | array | Array of frames for this sprite, where each frame is a struct containing information on its texture (more information under "Bitmap Sprite Data") |

**These additional variables are available only for Spine sprites:**

|                                                                                                                                            |         |                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------|
|  [Sprite Info Struct](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Information/sprite_get_info)  |         |                                                                                                    |
| Variable                                                                                                                                   | Type    | Description                                                                                        |
| **num_atlas**                                                                                                                              | real    | The number of atlas textures used                                                                  |
| **atlas_texture**                                                                                                                          | array   | Array of texture IDs used for the atlas                                                            |
| **premultiplied**                                                                                                                          | boolean |  true if this sprite is marked as premultiplied, otherwise false                                   |
| **animation_names**                                                                                                                        | array   | Array containing the names of each animation in this sprite                                        |
| **skin_names**                                                                                                                             | array   | Array containing the names of each skin in this sprite                                             |
| **bones**                                                                                                                                  | array   | Array containing structs for each bone in this sprite (more information under "Spine Sprite Data") |
| **slots**                                                                                                                                  | array   | Array containing structs for each slot in this sprite (more information under "Spine Sprite Data") |

The function will return undefined if the given sprite doesn't exist.
Also note that information returned in this struct should be considered
**read-only** as modifying any of these variables will not affect the
sprite. The sections below contain information on the arrays and structs
included in the returned struct based on the sprite type: [ General
Sprite Data General Sprite Data ](#) This section contains information
on variables included in the struct for all kinds of sprites. The
messages variable is an array that contains information on the broadcast
messages that exist in the given sprite. Each broadcast message in this
array is a struct containing the following variables:

|               |           |                                                                                  |
|---------------|-----------|----------------------------------------------------------------------------------|
| Variable Name | Data Type | Description                                                                      |
| **frame**     | real      | The timing of this broadcast message from the start of the animation (in frames) |
| **message**   | string    | The broadcast message string                                                     |

The frame_info variable is an array that contains information on the
timings of the sprite's frames. Each frame in this array is a struct
containing the following variables:

|                 |           |                                                    |
|-----------------|-----------|----------------------------------------------------|
| Variable Name   | Data Type | Description                                        |
| **frame**       | real      | The timing for the start of this frame (in frames) |
| **image_index** | real      | The image index of this frame                      |

[ Bitmap Sprite Data Bitmap Sprite Data ](#) This section contains
information on variables included in the struct for Bitmap sprites
(sprites that are not Spine or SWF type sprites). The frames variable is
an array that contains information on the textures of the sprite's
frames. Each frame in this array is a struct containing the following
variables:

|                     |           |                                                                                                                                                                                                 |
|---------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Variable Name       | Data Type | Description                                                                                                                                                                                     |
| **x**               | real      | The X position of this frame on its texture page (in pixels)                                                                                                                                    |
| **y**               | real      | The Y position of this frame on its texture page (in pixels)                                                                                                                                    |
| **w**               | real      | The logical width of the frame (in pixels) used internally                                                                                                                                      |
| **h**               | real      | The logical height of the frame (in pixels) used internally                                                                                                                                     |
| **texture**         | real      | The texture page ID for this frame                                                                                                                                                              |
| **original_width**  | real      | The original width of the frame (in pixels)                                                                                                                                                     |
| **original_height** | real      | The original height of the frame (in pixels)                                                                                                                                                    |
| **crop_width**      | real      | The actual width of the frame on the texture page after cropping and scaling (since GameMaker automatically trims the empty space around an image, and also scales it down if it doesn't fit)   |
| **crop_height**     | real      | The actual height of the frame on the texture page after cropping and scaling                                                                                                                   |
| **x_offset**        | real      | The X offset from the left edge of the original image to the left edge of the cropped section                                                                                                   |
| **y_offset**        | real      | The Y offset from the top edge of the original image to the top edge of the cropped section                                                                                                     |

[ Spine Sprite Data Spine Sprite Data ](#) This section contains
information on variables included in the struct for Spine sprites. The
bones variable is an array that contains information on all bones in the
given Spine sprite. Each bone in this array is a struct containing the
following variables:

|                    |           |                                                                                |
|--------------------|-----------|--------------------------------------------------------------------------------|
| Variable Name      | Data Type | Description                                                                    |
| **parent**         | string    | The name of the parent bone, or undefined if this bone doesn't have a parent   |
| **name**           | string    | The name of this bone                                                          |
| **index**          | real      | The index of this bone                                                         |
| **length**         | real      | The length of this bone                                                        |
| **x**              | real      | The X position of this bone                                                    |
| **y**              | real      | The Y position of this bone                                                    |
| **rotation**       | real      | The rotation of this bone                                                      |
| **scale_x**        | real      | (Internal to Spine) Scale value on X                                           |
| **scale_y**        | real      | (Internal to Spine) Scale value on Y                                           |
| **shear_x**        | real      | (Internal to Spine) Shear value on X                                           |
| **shear_y**        | real      | (Internal to Spine) Shear value on Y                                           |
| **transform_mode** | real      | (Internal to Spine) The transform mode                                         |

**NOTE** : Please consult the [Spine
documentation](http://en.esotericsoftware.com/spine-documentation) for
more information regarding Spine's internal variables. The slots
variable is an array that contains information on all slots in the given
Spine sprite. Each slot in this array is a struct containing the
following variables:

|                  |           |                                                                              |
|------------------|-----------|------------------------------------------------------------------------------|
| Variable Name    | Data Type | Description                                                                  |
| **name**         | string    | The name of the slot                                                         |
| **index**        | real      | The index of the slot                                                        |
| **bone**         | string    | The name of the slot's bone, or "(none)" if there is no bone for this slot   |
| **attachment**   | string    | Attachment name                                                              |
| **red**          | real      | Red component of the slot's colour (0-1)                                     |
| **green**        | real      | Green component of the slot's colour (0-1)                                   |
| **blue**         | real      | Blue component of the slot's colour (0-1)                                    |
| **alpha**        | real      | Alpha component of the slot's colour (0-1)                                   |
| **blendMode**    | real      | (Internal to Spine) Blend mode for the slot                                  |
| **dark_red\***   | real      | Red component of the slot's **dark** colour (0-1)                            |
| **dark_green\*** | real      | Green component of the slot's **dark** colour (0-1)                          |
| **dark_blue\***  | real      | Blue component of the slot's **dark** colour (0-1)                           |
| **dark_alpha\*** | string    | Alpha component of the slot's **dark** colour (0-1)                          |

\* **NOTE** : The dark color variables are only available if the slot
has [Tint Black](http://en.esotericsoftware.com/spine-slots#Tint-black)
enabled.

#### Syntax:

``` gml
sprite_get_info(index);
```

|          |                                                                   |                                                     |
|----------|-------------------------------------------------------------------|-----------------------------------------------------|
| Argument | Type                                                              | Description                                         |
| index    |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)  | The index of the sprite to get the information for. |

#### Returns

``` gml
 Sprite Info Struct

(or

 undefined

)
```

#### Example:

``` gml
var _info = sprite_get_info(sprite_index);

if (_info != undefined &amp;amp;&amp;amp; _info.type == 0)
{
    var _messages = _info.messages;
    var _messageCount = array_length(_messages);
    
    for (var i = 0; i &amp;lt; _messageCount; i ++)
    {
        var _message = _messages[i];
        show_debug_message("Message at frame " + string(_message.frame) + ": " + _message.message);
    }
}
```

The above code gets the info struct for the instance's sprite, and then
checks if it's not undefined and that its type is 0 (meaning that it's a
bitmap sprite). In that case, it gets the broadcast message array for
that sprite and then runs a for loop to print each broadcast message
(along with its frame) to the output log.
