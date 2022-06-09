# The Tile Set Brush Builder

By default when you "paint" tiles onto a tile map layer in the room
editor, you select a single tile and paint with that. However, tile sets
are almost always designed to have sections that fit together in
different ways to form whole areas or items. For example, an RPG tile
set may have landscape feature tiles that can be connected to create
larger or smaller features - like trees and buildings - depending on the
number of tiles used. Now, placing multiple features like this on a room
layer would require you to go back and forth many times to change tile,
which is not good for your workflow. To resolve this, GameMaker enables
you to create tile **Brushes** in the Tile Set editor, available when
you click  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
on the **Brush Builder** button:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Tilesets_Brushes.png)  
In the **Brush Builder** you have the original tile set on the left and
a blank "canvas" on the right. You can now select any tile from the left
and paint it on the right to create custom "brushes" which you can then
use in the room editor. Note that you can click and hold the left mouse
button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
then drag on the tile set to select multiple tiles to paint into the
brush canvas and you can also hold down  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
/  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
+  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
to add specific individual tiles or hold down  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Alt.png)  
+  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
to remove specific tiles. The following image shows our previously
mentioned landscape features as an example of three custom brushes made
from a single tile set:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Tilesets_FeaturesBrushes.png)  
On the right you can see three features that we've made (highlighted
with an orange box in the image). Notice how we've left a gap of one
tile between each feature - this is because *any touching group of tiles
will be treated as a single brush* in the room editor, so we leave a gap
of one tile to show that each set is a distinct brush we want to create.
While creating your brushes, you paint with the left mouse button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
and delete with the right mouse button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RMB.png)  
. You can also zoom the tile sheet or the brush canvas using  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
/  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
and the mouse wheel  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_MMB.png)  
when the mouse is over one of the windows, or you can pan around using  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Space.png)  
+  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
or the middle mouse button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_MMB.png)  
and dragging. Note that you can also use the zoom tools in the
**Toolbox** within the editor windows to change the zoom levels of
either window as well as toggle the grid visibility and colour. At the
top right you can see the currently selected tool, and you can also set
the size of the brush that you want to paint with. The default size is
1, which is a single tile, but if you set it to higher values then you
can paint (and erase) with a larger brush composed of the selected tile
repeated, as shown in the image below:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Tilesets_Tile_Size.gif)  
The toolbox is where you can select the tool to use for many different
tasks in the Tile Set editor, some of which will depend on whether you
have anything defined in your [auto tile](Auto_Tiles) library. A
brief outline of each tool is given below (note that when you have
selected a tile layer in the Room Editor, then this toolbox is displayed
at the top of the room workspace, along with additional drawing tools):

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
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Tile_Draw.png" /><br />
</td>
<td><strong>Pencil</strong></td>
<td>This is the pencil tool. It uses the selected tile to paint in the
Brushes window with the left mouse button<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png" /><br />
and you can erase with the right mouse button<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RMB.png" /><br />
.</td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Tile_Erase.png" /><br />
</td>
<td><strong>Eraser</strong></td>
<td>With the eraser tool you can use the left mouse button<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png" /><br />
to erase a given tile in the Brushes window. Essentially, all this does
is set the tile index to 0, which is the reserved "empty" tile.</td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_TileSelect.png" /><br />
</td>
<td><strong>Selection</strong></td>
<td>This is the selection tool, which can be used to define an area of
the Brushes window for working on. You can click the left mouse
button<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png" /><br />
and then drag the mouse to create a rectangular area, or you can
press<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png" /><br />
/<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png" /><br />
+<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png" /><br />
to add multiple selections and<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Alt.png" /><br />
+<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png" /><br />
to clear a part of the selection. To clear the whole selection you can
press<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Escape.png" /><br />
. When you have an area of a Brushes window selected, the rest of the
tools (Pencil, Flip, Rotate, etc...) will only work within the selected
area. Note that you can also select tiles in the window then copy
(<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png" /><br />
/<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png" /><br />
+ " <span> C </span> "), cut (<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png" /><br />
/<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png" /><br />
+ " <span> X </span> ") and paste (<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png" /><br />
/<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png" /><br />
+ " <span> <strong>V</strong> </span> ") them, which will then switch
the tool to the Pencil and permit you to "paint" with them.</td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Tile_Auto.png" /><br />
</td>
<td><strong>AutoTile</strong></td>
<td>Clicking this tool enables the <strong>Auto tiling</strong> paint
style. When this is active you can select any tile from the Autotile
Libraries tab, and then paint it into the Brushes window and <span>
GameMaker </span> will automatically change it to match the surrounding
tiles, as long as you have correctly set up the <a
href="Auto_Tiles">Auto Tile Tab</a> . Note that selecting a tile
from the tile set that is not part of the autotile libraries will reset
the drawing tool to the standard Pencil tool.</td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Tile_Flip.png" /><br />
</td>
<td><strong>Flip</strong></td>
<td>Clicking the Flip tool with the left mouse button<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png" /><br />
(or using the keyboard shortcut " <span> X </span> " ) will flip the
tile or tiles currently selected for drawing along the
<em>horizontal</em> axis, without changing drawing tool (if you have a
custom brush selected for drawing, the whole brush will flip). If you
have no tile selected for drawing, but do have a group of tiles selected
in the brush window, then the flip tool will Flip the selected
tiles.</td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Tile_Mirror.png" /><br />
</td>
<td><strong>Mirror</strong></td>
<td>Clicking the Mirror tool with the left mouse button<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png" /><br />
(or using the keyboard shortcut " <span> Y </span> " ) will mirror the
tile(s) currently selected for drawing along the <em>vertical</em> axis,
without changing drawing tool (if you have a custom brush selected for
drawing, the whole brush will mirror). If you have no tile selected for
drawing, but do have a group of tiles selected in the brush window, then
the Mirror tool will mirror the selected tiles.</td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Tile_Rotate.png" /><br />
</td>
<td><strong>Rotate</strong></td>
<td>Clicking the Rotate tool with the left mouse button<br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png" /><br />
(or using the keyboard shortcut " <span> Z </span> " ) will rotate the
tile(s) currently selected for drawing 90° <em>clockwise</em> , without
changing drawing tool (if you have a custom brush selected for drawing,
the whole brush will rotate). If you have no tile selected for drawing,
but do have a group of tiles selected in the brush window, then the
Rotate tool will rotate the selected tiles.</td>
</tr>
</tbody>
</table>

Below the tools, you can find two different sections for selecting any
[**auto tile**](Auto_Tiles) or [**animated**
tiles](Animated_Tiles) that have been created using the current tile
set image. A single sprite that is used for a tile set can have many,
many, single cell images in it, and these can be combined in the
Animation or Autotile editor to create custom brushes which will show up
in these sections and can be used in conjunction with regular static
tiles to create brushes (note that an animated tile will animate
regardless of whether you have selected it from the library or from the
base tile set). Once you have set up all the brushes you require, you
can then use them to paint tiles onto any tile map layer within the
[Room Editor](../Rooms) .
