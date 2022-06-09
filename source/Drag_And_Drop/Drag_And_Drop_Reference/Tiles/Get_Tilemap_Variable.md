#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Tiles/i_Tiles_Get_Tilemap_Variable.png) Get Tilemap Variable

With this action you can retrieve any one of a given number of variables
for the tile map element on a layer. When you create a tile layer in the
room editor, this layer holds a **tile map element** which is then
populated with tiles from a tile-set. This tile map element has certain
values associated with it, like an offset position, the tile-set being
used, the width, height, etc... The complete list of values that you can
get is:

-   [X
    Coordinate](../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/tilemap_get_x)
    : The position along the x axis on the layer where the tile map
    element has been placed.
-   [Y
    Coordinate](../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/tilemap_y)
    : The position along the y axis on the layer where the tile map
    element has been placed.
-   [Columns](../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/tilemap_get_width)
    : The width (defined as the number of columns of tile cells) of the
    tile map element.
-   [Rows](../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/tilemap_get_height)
    : The height (defined as the number of rows of tile cells) of the
    tile map element.
-   [Tile
    Width](../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/tilemap_get_tile_width)
    : The width of a single tile cell.
-   [Tile
    Height](../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/tilemap_get_tile_height)
    : The height of a single tile cell.
-   [Tile Set
    Resource](../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/tilemap_tileset)
    : The tile-set resource that has been assigned to the tile map
    element for drawing.
-   [Current
    Frame](../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/tilemap_get_frame)
    : The current frame being drawn for animated tiles.
-   [Mask](../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/tilemap_get_mask)
    : The mask data for the tile map element.
-   [Global
    Mask](../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Tile_Map_Layers/tilemap_get_global_mask)
    : The global mask data for all tile map elements.

When using this action you supply the layer name (a string, as defined
in the Room Editor) to get the tile map element data from, then the type
of data that you want to retrieve (as shown in the list above). The
returned value will then be stored in the target variable which can have
been created previously or can be a new temporary one (if you check the
"Temp" check-box). Note that you can retrieve additional values by
clicking the plus icon   
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Icon_Expand_Arguments.png)  
beside the action, and selecting another variable and giving another
variable to store the returned value.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Tiles/a_Tiles_Get_Tilemap_Variable.png)  

#### Arguments:

|          |                                                         |
|----------|---------------------------------------------------------|
| Argument | Description                                             |
| Layer    | The layer to get data from                              |
| Variable | The variable to retrieve the value of (as listed above) |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Tiles/e_Tiles_Set_Tile_Set.png)  
The above action block code checks to see if the tiles on the layer
"Floor_Tiles" is using the tile-set "tl_PalaceRuins", and if they not,
then they are set to use it.
