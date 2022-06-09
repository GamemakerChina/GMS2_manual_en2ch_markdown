# Texture Pages

When you create a game with GameMaker , you will surely have created
graphics - sprites, tilesets and fonts - to go along with it. These
graphics are stored on **Texture Pages** which GameMaker builds for you
from all the image resources that your game contains. Below is an
example of a completed texture page:  
![](https://gms.magecorn.com/Manual/assets/Images/Settings/Texture_Page_Example.png)  
As you can see, the game graphics are all jumbled up together in such a
way that they all fit on a power of 2 sized page, eg 512x512, 1024x512
etc... up to a maximum size of 4096x4096 pixels page. Note that the
maximum size of a texture page will depend on the chosen export
platform, as some targets will not permit pages larger than 2048x2048px,
and even then, the maximum available size may not be optimal for all the
devices that use the target platform OS. Note too that if your images
have a lot of empty space (ie: transparent pixels) around them, then
they will be cropped by default to remove any of these "invisible"
pixels and pack as many images as possible onto a single texture page.
If this is not what you wish to happen, then you need to disable it from
the [Texture Groups](../Texture_Groups) window. It is important to
understand how the different available texture settings will affect an
image, so lets look at the [Sprite
Editor](../../The_Asset_Editors/Sprites) section titled **Texture
Settings** , shown below:  
![](https://gms.magecorn.com/Manual/assets/Images/Settings/Texture_Page_Options.png)  
Here you can define how the image is to be stored on the texture page as
well as whether it is an image specifically for use with 3D and has to
be stored separately and which texture page (if any) it has to be
assigned to as well as a few other options (explained in epth on the
[Sprite Editor](../../The_Asset_Editors/Sprites) page). The options
we are interested in are the first two: Tile Horizontal and Tile
Vertical. These relate to how the edges of the image will be created
when placed on the texture page. An image that is to be tiled will have
the edges (horizontal or vertical) added to by the edges from the
opposite side, while if no tiling is selected the sprite will be
*clamped* and the edges pixels will be repeated (note that tilesets also
have a setting for the output border width, found in the [Tile Set
Properties](../../The_Asset_Editors/Tile_Sets) which does the same
thing, only for each tile in the set). The following image illustrates
this:  
![](https://gms.magecorn.com/Manual/assets/Images/Settings/Texture_Page_Results.png)  
Underneath those settings is the **Separate Texture Page** setting. This
option will force GameMaker to place this image on its own unique
texture page and there are no options associated with this as the tiling
or clamping is controlled directly through code. This is most commonly
used for texturing 3D models (in which case the texture should be a
power of 2, eg: 128x128, 512x512, 256x1024, etc...), but you can use it
to force any image to be drawn to its own unique page. **NOTE** : Take
care when using this option as you can quickly use up all the available
texture memory, especially on mobile devices, if you have too many
texture pages. Now, when your game is large with a lot of artistic
resources, it may be that the way GameMaker automatically creates these
pages is not the optimum for getting the most out of the target device,
due to the fact that if a room in your game needs resources from 4
different texture pages, the device will have to swap these pages into
(and out of) memory constantly, which may cause a loss in performance.
To that end, you have the option to tell GameMaker what images are to be
placed on any specific texture page by assigning them to specific
**Texture Groups** . The final aim of this is to minimise the number of
swaps being done in a game at any one time (texture pages can added from
the [Texture Groups](../Texture_Groups) window). It should be noted
that in the individual platform tabs that can be found in the [Game
Options](../Game_Options) there is a button that permits you to view
the texture pages that you have defined, just as they would be created
for each target. This is very handy for working out how many pages are
being created and what's on them. Should you have a texture in your game
that is larger than the maximum selected texture page size, then this
will be *scaled down by half* (and half again if necessary) until it
fits on the maximum page size. It will *not* be split into sections over
various texture pages. This means that when you test your game on
Windows, Ubuntu (Linux) or MacOS the game may look fine as you are using
larger texture pages, but on iOS (or any of the other targets that
require a smaller texture page size for optimal performance) the texture
may look blurred or have artefacts. It is essential that you make sure
your images are all able to fit on the smallest of the texture page
sizes that your game will use, and if not then you should split them
into smaller images and then draw them together in your game to give the
illusion of one large, complete, image. **NOTE** : Before you go off
splitting up your graphics over various texture pages, you should be
aware that this is not always necessary, nor is it always the most
efficient way to work. Some games may be more CPU bound than GPU bound
(see the section on [Debugging](../../Introduction/Debugging) for
more information) and those games will not benefit greatly from this
optimisation, and you should also consider whether it would not be
better to have all your images on two texture pages and swap between
them rather than spread out over several, which is just wasting memory.
