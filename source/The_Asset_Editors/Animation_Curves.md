# The Animation Curve Editor

  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Animation_Curves.png)  
An animation curve is an asset that contains one or more curves that
represent how a value changes over time, and can use linear
interpolation , smooth interpolation or bezier interpolation to go
between different points in the curve. The values you set on the
vertical axis can be between any two values (between -1 and 1 by
default) and the duration along the horizontal axis is *always*
normalised from 0 to 1, making it easy to target different time ranges
using multipliers in your game code or stretch them to fit a track in
the [Sequences Editor](Sequence_Properties/Using_Animation_Curves) .
Animation curves are comprised of "channels" and each channel can have
its own curve settings, which permits you to - for example - describe a
spatial position with two channels for the x/y location, or a colour
gradient with 4 channels to represent a colour format. Animation curve
assets can be used when working with Sequences and can also be accessed
using code, making them a powerful tool when creating your games. When
you first create an animation curve asset the editor window will open
and present you with the following sections: [ Curve Name Curve Name
](#) Here you can give your animation curve a unique name ( alphanumeric
characters and the "\_" underscore symbol only ). This name is what will
be used to refer to the curve and all its channels when accessing it
through code or in a sequence. [ Curve Library Curve Library ](#) The  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Animation_Curve_Library_Button.png)  
button opens the ** Animation Curve Library ** window, which allows you
to change the Curve Type of the Animation Curve, and apply a preset to
the selected channel.  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Animation_Curves_Library.png)  
See the section on [Animation Curve
Library](Animation_Curve_Properties/Animation_Curve_Library) for
information on Curve Types and Presets. Note that opening the window
through the  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Animation_Curve_Library_Button.png)  
button will have the **"Overwrite"** Apply Mode selected by default. [
Channel List Channel List ](#) The channel list is where you can add and
name the different channels that will comprise your animation curve
asset. By default when you first create an animation curve, a channel
will have been added for you and you can add further channels by
clicking on the  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Animation_Curves_New_Channel.png)  
button to the left of the curve name. Each channel must have a unique
name (using alphanumeric characters and the "\_" underscore symbol only
), and you can also set the colour for the channel by double clicking  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
on the colour swatch to the left, which will open the colour picker to
let you choose a new colour. To rename the channel, you can do a slow
double click  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
and rename, and you can also use the right mouse button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RMB.png)  
to open a menu where you can choose to rename, change the colour or
delete the channel. Channels can be expanded by clicking on the arrow
beside the name to show each of the points on the channel curve, and
these points can be edited manually by clicking the current value and
typing in the new value.  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Animation_Curves_ExpandList.png)  
You can toggle the channel visibility by clicking on the "eye" icon  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_ToggleVisibility.png)  
, or delete the channel by clicking the "bin" icon  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_DeleteChannel.png)  
. [ Channel Range Channel Range ](#) The Channel Range button is used
for setting the visual vertical range for the Channel Editor. By default
this will be set from -1 to 1, but clicking this button will open the
following window:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Animation_Curves_Range.png)  
Changing these values will change the way the data is represented in the
Channel Editor section, permitting you to have higher/lower values along
the channel curve than just -1 to 1. Note that this is purely visual and
does not clamp the values for the channel. [ Channel Editor Channel
Editor ](#) The Channel Editor shows a visual representation of the
different channels used in the animation curve. By default, all channels
will be shown here, but you can only edit the channel currently selected
from the Channel List, which will be highlighted in the editor. You can
change the position of any of the points along the channel curve by
clicking  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
on them and dragging them around within the editor, but note that the
first and last point can only be changed along the vertical axis and
their horizontal value will always be 0 and 1 respectively. You can add
points directly to the channel curve by moving the mouse close to the
main channel line and then clicking  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
when the cursor changes to the " **Add Point** " tool, and you can then
edit these points by clicking  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
and dragging or by changing their values in the expanded channel options
in the Channel List:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Animation_Curves_Channel_Editor.gif)  
You can edit multiple points at once by clicking  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
and dragging within the editor to select all the points you want to edit
or by using  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
/  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
+  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
to add points to the selection individually. Releasing the mouse button
and then clicking again on any of the points in the selection and
dragging will move them all together:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Animation_Curves_Channel_Editor_Moving.gif)  
You can  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RMB.png)  
right-click anywhere in the Channel Editor to open the [Animation Curve
Library](Animation_Curve_Properties/Animation_Curve_Library) window
(only when the selected Curve Type is **Bezier** ). Applying a preset in
this way will affect the whole channel. To modify only a part of the
channel, you can  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RMB.png)  
right-click on an individual line to apply a preset to it, or select
multiple lines by clicking  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
and dragging, then  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RMB.png)  
right-click on the selection to apply a preset to the selected lines.  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Animation_Curves_Channel_Editor_Presets.gif)  
Note that opening the **Animation Curve Library** window through the
Channel Editor will have the **"Between"** Apply Mode selected by
default. [ Zoom Controls Zoom Controls ](#) The zoom controls permit you
to expand  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_ZoomOut.png)  
or contract  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_ZoomIn.png)  
the vertical scale of the channel curves in the Channel Editor. You can
also click the "Center Fit" button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_CenterFit.png)  
to have the Channel Editor view adjust it's scale to fit all the points
on the channel curve within the editor, centered around the mid range of
the values:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Animation_Curves_Zoom.gif)  
For information on the different Runtime functions that can be used
along with animation curves, please see the following section of the
manual:

-   [Animation Curve
    Functions](../GameMaker_Language/GML_Reference/Asset_Management/Animation_Curves/Animation_Curves)
