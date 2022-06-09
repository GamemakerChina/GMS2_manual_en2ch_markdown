# Text in Sequences

Text tracks can be added to a Sequence through the editor. This is done
by selecting the  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_TextButton.png)  
**Add a Text Track** button from the Canvas Toolbox, and then clicking
(and optionally dragging) in the Canvas to create a text track.  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Sequences_Text/SeqTextOverview.png)  
This page covers the following topics:

1.  [Creating Text](#s1)
2.  [Modifying Text](#s2)
3.  [Font Assets](#s3)
4.  [Parameters](#s4)
5.  [Inspector](#s5)

## Creating Text

There are two ways of creating a text track. After selecting the  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_TextButton.png)  
**Text** tool from the Toolbox, you can:

-   **Click once in the canvas** : This creates an "unwrapped" text
    track. This means the text can be as long as you want and it will
    stay on one line. Wrapping can easily be enabled later through the
    [Inspector](../../IDE_Tools/The_Inspector) .
-   **Click and drag in the canvas** : This creates a "wrapped" text
    track, meaning the text only displays inside a frame. The size of
    this frame is set by dragging while creating the text track. Its
    size can also be changed later via parameter tracks or the
    Inspector.
    It is recommended to use wrapped text tracks as it makes it much
    easier to align your text and get consistent results while
    animating.

## Modifying Text

When you create a new text track, GameMaker opens the
[Inspector](../../IDE_Tools/The_Inspector) and automatically selects
the **Text** field, allowing you to start writing your text.  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Sequences_Text/SeqTextEditFromInspector.png)  
To edit the text for a track at any time, simply select that track, go
into the Inspector and modify the **Text** field again. Resize Behaviour
Resizing your text track in the Canvas will work differently depending
on whether your text track is **wrapped** or **unwrapped** . If
unwrapped, your text track will be scaled, similar to how you scale
sprites and objects. However, resizing a **wrapped** text track modifies
its **frame size** instead of modifying its scale values.  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Sequences_Text/SeqTextResizeBehaviour.png)  
To scale a wrapped text track, use
[Gizmos](The_Sequence_Canvas#gizmos) instead, or edit the values in
the Scale parameter track manually.

## Font Assets

Text tracks are tied to [Font assets](../Fonts) . When you create a
new text track, it will look for a font asset within your project, and
use the one that was last added. If your project has no fonts, it will
automatically create a new font asset. When you delete a font, all text
tracks that use that font are deleted as well, so ensure you don't
accidentally delete font assets that are used in Sequences.

## Parameters

You can modify and animate all the usual parameters that are provided
for a sprite track, like Position, Rotation, Scale, Origin and Colour
Multiply. Using these parameters you can move and rotate your text, make
it bigger or smaller, and change its colour and alpha. There are some
text-specific parameters provided as well, which can also be animated:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Sequences_Text/SeqTextParameters.png)  

-   **Character Spacing** : This is the space between each character (in
    pixels).  
    ![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Sequences_Text/SeqTextCharacterSpacing.png)  
-   **Line Spacing** : This is the space between each line of text (in
    pixels).  
    ![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Sequences_Text/SeqTextLineSpacing.png)  
-   **Paragraph Scaling** : This is the space between each paragraph of
    text (in pixels). A new paragraph starts when you add a line break
    manually by pressing  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Enter.png)  
    .  
    ![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Sequences_Text/SeqTextParagraphSpacing.png)  
-   **Frame Size** : This is the size of the text's frame, and is only
    used when **Wrap** is enabled in the Inspector (see its section
    below for more information).

## Inspector

There are some properties that can only be changed through the
Inspector. Such properties cannot be animated as they are not parameter
tracks, but simple options that apply to the whole track. The Inspector
shows you the following properties when a text track is selected: NOTE
The Inspector should open automatically when you create or select a text
track, but if your Inspector is closed, you can open it manually from
the [Windows](../../IDE_Navigation/Menus/The_Windows_Menu) menu at
the top.  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Sequences_Text/SeqTextInspector.png)  
Some of the parameter tracks (such as **Colour** , **Character Spacing**
, **Line Spacing** , etc.) are included here, and changing them will
create a keyframe at the playhead if  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Seq_Record.png)  
**Automatically record changes** is enabled, or modify the selected
keyframe. The rest of the options are "static" (as they cannot be
animated) and are as follows:

-   At the top it shows you the font asset that is selected. You can use
    this option to select an existing font asset, or create a new one
    and assign it to the selected text track.
-   **Text** : This is the text that is displayed on your text track.
    You can enter multiple lines here, however empty lines will not be
    displayed.
-   **Alignment** : Here you can change how your text is aligned within
    the frame horizontally (left, centre, right, justified) and
    vertically (bottom, top, middle). This only applies when the
    **Wrap** option is enabled.
-   **Wrap** : This controls whether the text should automatically wrap
    within the defined frame. When this is enabled, your text will
    automatically move to the next line when it hits the end of the
    frame, and will always be cut off if the text happens to be longer
    than the height of the frame. When this is disabled, all of your
    text will be displayed on a single line, and the frame will not be
    displayed in the canvas anymore.
