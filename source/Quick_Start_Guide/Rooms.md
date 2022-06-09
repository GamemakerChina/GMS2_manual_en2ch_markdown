# Rooms

All games that you make in GameMaker need at least one room to run (but
can have many, many more) , and a room is just a space where you place
instances of the objects that make up your game as well as tiles and any
other graphical resources. When you first create a room in the [Asset
Browser](../Introduction/The_Asset_Browser) you will be presented
with a new [**Room Editor**](../The_Asset_Editors/Rooms) workspace
with which to edit its properties, something like this:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_RoomEditor.png)  
By default the room tools will be placed on the left, with three main
sections:

-   **Layer Editor** : Everything in a room is placed on *layers* , and
    there are different layer types that you can choose from (more on
    this later). Layers are ordered by *depth* and this depth is what
    defines the order in which the layer contents will be rendered to
    the screen when the game runs. Depth ordering is from highest to
    lowest, so that the lower the depth the nearer the "camera" and the
    higher the depth the further away. For example, a layer with a depth
    of -300 will render over a layer with a depth of -100, and a layer
    with a depth of 1000 will render under everything with a depth less
    than this. Note that by default, GameMaker will order layer depths
    for you according to the position in the Layer Editor, and you can
    drag around layers using the mouse to re-order them and GameMaker
    will re-order the depths to match.
-   **Layer Properties** : Each layer that you add to the room will have
    its own properties, and those properties will change depending on
    the layer type. This window permits you to change those properties
    and edit how the layer will be rendered .
-   **Room Properties** : Rooms have a number of properties too, and
    these can be set here. Things like the room size, the camera view
    ports that are active and a few other things can be set here.

We've mentioned that there are different layer types, so let's just go
over what they are and how they can be used when building your games:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Layer_Background.png" /><br />
</td>
<td><strong>Background Layer</strong></td>
<td>The background layer is a layer that can be filled with a
<em>single</em> colour or a <em>single</em> image. It can be moved and
positioned within the room, and you can have multiple background layers.
Generally this is used, as the name suggests, to generate a constant
background for all the other layers in the room. By Default a new room
will always contain a background layer, but you can remove it if you
don't need it.</td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Layer_Instances.png" /><br />
</td>
<td><strong>Instance Layer</strong></td>
<td>The instance layer is where you place all the instances of the
objects that you require for the game. To add an instance to a layer,
simply click<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png" /><br />
on the object in the asset browser and then drag it into the room editor
workspace. When you release the mouse button, an instance of that object
will have been added to the room. By Default a new room will always
contain an instance layer, but you can remove it if you don't need
it.</td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Layer_Tilemap.png" /><br />
</td>
<td><strong>Tile Map Layer</strong></td>
<td><span> After having created a <span>tile sets</span> , you need to
add the tiles to your room, which is done by creating a <span>tile
map</span> layer. A tile map layer is a layer that permits you to add
tiles from any of the tile set assets that you have created and will be
set up automatically to use a grid the size of the tile set cells. You
can only add a single tile to each grid cell, so if you require multiple
tiles to occupy the same space, then you should be using multiple tile
map layers. </span></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Layer_Path.png" /><br />
</td>
<td><strong>Path Layer</strong></td>
<td><span> The path layer is the only one that does not actually get
rendered when you run your game. This layer is more of a "convenience"
layer for helping you to create or edit <strong>Path</strong> assets,
since it permits you to add or edit paths within the actual room space.
</span></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Layer_Asset.png" /><br />
</td>
<td><strong>Asset Layer</strong></td>
<td>Sometimes you want a nice graphical effect but don't want the
overhead of using an instance or don't need it to do anything other than
draw itself. You could use a tile map, but given that tile maps are
restricted to using a grid and only a single image per grid cell, they
can be a bit restrictive. This is when you would use the asset layer.
The asset layer simply takes a sprite resource and draws it using the
parameters that you set when you add it into the room. Sprites and
sequences can be added to this layer the same way that instances of
objects are added to the instance layer, ie: you click<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png" /><br />
on the sprite in the asset browser and then drag it into the room editor
workspace.</td>
</tr>
</tbody>
</table>

We won't go into much more details about the room editor here (for that
we have [this section](../The_Asset_Editors/Rooms) of the manual),
but we will briefly explain how to add instances to an Instance Layer,
as you'll need to know that for the next section of the Quick Start
Guide. To add an instance to the room editor, you must first select an
Instance Layer from the Layer Editor on the left (or create one if none
exist). You can then go to the Asset Browser and simply click  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
and drag an object that you want from there and drop it into the room at
the position you want, which will add a single instance of that object
to your game:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_AddingInstances.gif)  
If you want to place multiple instances in the room, then you can select
an object from the resource tree and then press and hold  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Alt.png)  
to preview the resource, and if you additionally click the left mouse
button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
you can then "paint" it into the room layer.  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_PaintingInstances.gif)  
Note that assets are given a position when they are added into the room
editor based on their X and Y axis positions relative to the room
**origin** . The room origin is the (0, 0) position, which in GameMaker
is the top let corner, and to the right is +X and down is +Y, eg:  
![](https://gms.magecorn.com/Manual/assets/Images/QS_Guide/QS_RoomEditorAxis.png)  
In the above example the instance is placed in the middle of the room at
position (X:512, Y:384). It's also possible to go outside of the room
bounds and have positions that are greater than the room axis lengths,
or even less than than the room origin - in which case the X/Y
coordinates will be negative values. For more detailed information on
the Room Editor, you can see the following section of the manual:

-   [Editors: The Room Editor](../The_Asset_Editors/Rooms)

That wraps it up for the Room Editor in this Quick Start Guide, and you
should now know enough to actually get started creating sprites and
objects and designing rooms for them. The next sections of this guide
are going to cover some of the programming fundamentals to help you on
your way, starting with actually **Drawing** things to the screen.
