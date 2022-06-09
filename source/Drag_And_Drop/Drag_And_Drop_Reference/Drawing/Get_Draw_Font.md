#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/i_Drawing_Get_Font.png) Get Draw Font

With this action you can get the ID value of the font currently assigned
for drawing. The value returned will be either -1 for no font assigned,
or a value \>= 0 that represents a font constant from the Asset
Browser. The return value will be stored in the **target variable** that
you specify, which can have been created previously or can be a new
temporary one (if you check the "Temp" check-box).

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/a_Drawing_Get_Font.png)  

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Drawing/e_Drawing_Get_Font.png)  
The above action block code checks the current font being used for
drawing, and if it's not the given asset, then it is set to that asset.
