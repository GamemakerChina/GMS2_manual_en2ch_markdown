# tilemap_get_frame

Since tiles can be animated, it can sometimes be useful to know which
frame is currently being drawn and react accordingly, so with this
function you can retrieve the current frame index for a given tile map.
You give the tile map element ID (which you get when you create a tile
map element using [ layer_tilemap_create() ](layer_tilemap_create)
or when you use the function [ layer_tilemap_get_id()
](layer_tilemap_get_id) ), and the function will return the frame
index.

#### Syntax:

``` gml
tilemap_get_frame(tilemap_element_id)
```

|                    |                                                                                                                                             |                                                                       |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| Argument           | Type                                                                                                                                        | Description                                                           |
| tilemap_element_id |  [Tile Map Element ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/layer_tilemap_get_id)  | The unique ID value of the tile map element to get the frame index of |

#### Returns:

``` gml
 Real

(between 0 (inclusive) and the maximum number of frames of animation (exclusive))
```

#### Example:

``` gml
var lay_id = layer_get_id("Tiles_Traps");
var map_id = layer_tilemap_get_id(lay_id);
if tilemap_get_frame(map_id) &amp;gt;= 2 &amp;amp;&amp;amp; tilemap_get_frame(map_id) &amp;lt; 4
{
    global.activate = true;
}
else
{
    global.activate = false;
}
```

The above code checks the current animation frame for the given tile map
on the given layer, and sets a global variable based on the return
value.
