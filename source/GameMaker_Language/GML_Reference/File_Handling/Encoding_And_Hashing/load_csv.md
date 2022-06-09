# load_csv

This function will load a CSV format file and convert it into a DS grid,
returning the unique ID value for the grid created.

#### Syntax:

``` gml
load_csv(filename)
```

|          |                                                                           |                                            |
|----------|---------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                      | Description                                |
| filename |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the file to open (as a string) |

#### Returns:

``` gml
 DS Grid ID
```

#### Example:

``` gml
file_grid = load_csv("spreadsheet.csv");
var ww = ds_grid_width(file_grid);
var hh = ds_grid_height(file_grid);
var xx = 32;
var yy = 32;
for (var i = 0; i &amp;lt; ww; i++;)
{
    for (var j = 0; j &amp;lt; hh; j++;)
    {
        draw_text(xx, yy, string(file_grid[# i, j]));
        yy += 32;
    }
    yy = 32;
    xx += 32;
}
```

The above code will open the given CSV file and store the returned DS
grid in the variable "file_grid". This grid is then parsed in a couple
of for lops and the contents drawn to the screen.
