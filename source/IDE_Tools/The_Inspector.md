# The Inspector

The **Inspector** window shows all the properties associated with the
selected elements in the IDE. This window will show information about
the element(s) being inspected and allow you to change its various
properties:

![Inspecting Sequence
Track](https://gms.magecorn.com/Manual/assets/Images/IDE%20Tools/Inspector.png)

![Inspecting Sound
Asset](https://gms.magecorn.com/Manual/assets/Images/IDE%20Tools/Inspector_Sound.png)

It can be opened from [The Windows
Menu](../IDE_Navigation/Menus/The_Windows_Menu) at the top of the
GameMaker window, and you can open as many as you like:  
![](https://gms.magecorn.com/Manual/assets/Images/IDE%20Tools/Inspector_Opening_Windows.png)  
After opening an Inspector window, you can dock it anywhere in the IDE,
or use it as a floating window:  
![](https://gms.magecorn.com/Manual/assets/Images/IDE%20Tools/Inspector_Docking.gif)  

## Using the Inspector

The Inspector is very useful for viewing and editing assets without
having to rely solely on [Workspaces](../Introduction/Workspaces) .
For example, you may usually edit your object code in fullscreen, and
frequently navigate back into a Workspace to edit that object's
properties. With the Inspector, you can view an object's details while
remaining in fullscreen view:  
![](https://gms.magecorn.com/Manual/assets/Images/IDE%20Tools/Inspector_Object_Editing.png)  
This makes it possible to modify an object's properties
and delete/change events while editing its code in fullscreen, and also
set up Parenting, Variable Definitions, and more. While this particular
example only covers objects, the Inspector can do much more and allow
you to edit many different kinds of assets (e.g. Sprites, Fonts,
Animation Curves, etc.). You can also edit multiple assets at once, by
selecting your desired assets in the [Asset
Browser](../Introduction/The_Asset_Browser) and modifying their
properties in your currently active Inspector window.

### Room Layers

In addition to assets, you can also inspect specific elements in the
IDE, such as layers in a room. Using the Inspector on room layers allows
you to change its properties and apply a filter/effect to it:  
![](https://gms.magecorn.com/Manual/assets/Images/IDE%20Tools/Inspector_Room_Layers.png)  
NOTE When you apply a filter/effect to a non-FX layer using the
Inspector, it will always be applied as a "single layer" effect, i.e.
its effect will only be applied on that particular layer and not on
other layers below it.

## Multiple Inspectors

You can open multiple Inspector windows at any time, and each one can be
linked to a specific element in the IDE. To ensure that each time you
click an element all open inspectors don't change to show the new
selection, you must first **lock** each inspector window one-by-one. To
do this, you would open an inspector, select an IDE element to inspect,
and then click the  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Padlock.png)  
lock button on the inspector to lock it on the element (shown in the
image below). Once you have locked an inspector, you can open another
one and then repeat the process.  
![](https://gms.magecorn.com/Manual/assets/Images/IDE%20Tools/Inspector_Lock.png)  
Note that a locked inspector window does not lock the editing of any
values for the element being inspected. It simply locks the inspector to
the selected element and you can continue to edit it at any time, even
when the original element is not the main focus of the IDE. Using the
lock feature you can open multiple inspectors at the same time with each
one being locked to a specific asset, as shown in the example below:  
![](https://gms.magecorn.com/Manual/assets/Images/IDE%20Tools/Inspector_Multiple.png)  
