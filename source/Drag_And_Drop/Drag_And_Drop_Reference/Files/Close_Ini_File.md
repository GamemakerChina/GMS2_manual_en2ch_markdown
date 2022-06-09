#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/i_Files_Close_Ini_File.png) Close Ini File

This action will close the currently open Ini file. This action should
be called the moment you are finished reading or writing to any open Ini
file (Ini files are opened using the action [Open Ini
File](Open_Ini_File) ). If you do *not* use this action after you
have used the [Write To Ini File](Write_To_Ini_File) action, then
nothing will be written to disk as the file information is held in
memory until this action is called, at which point it is taken from
memory and written to the file on disk. Also note that if you try to
open an Ini file without having previously closed another one (or the
same one) you will get an error.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/a_Files_Close_Ini_File.png)  

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/e_Files_Open_Ini_File.png)  
The above action block code will open an ini file for use, then get the
value associated with the "name" key under the "player" header. If the
name returned matches the default name value (ie: the file, section or
key does *not* exist) then the file has a global variable written to it
before being closed (and writing the new data to disk).
