#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/i_Files_Delete_File.png) Delete File

With this action you can delete a file that has been created previously.
You supply the file name (as a string) of the file to be deleted. Note
that you *cannot* delete any files that are included in the game bundle,
only those that have been created using the [Close
Ini](Close_Ini_File) or [Save Buffer](Save_Buffer) actions (see
the section on [The File
System](../../../Additional_Information/The_File_System) for more
information).

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/a_Files_Delete_File.png)  

#### Arguments:

|          |                                              |
|----------|----------------------------------------------|
| Argument | Description                                  |
| Filename | The name (as a string) of the file to delete |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/e_Files_Rename_File.png)  
The above action block code will check to see if the file
"checkpoint.sav" exists, and if it does it then checks to see if the
file "checkpoint_OLD.sav" exists. If that file exists as well, then it
is deleted, and then the original "checkpoint.sav" file is renamed to
"checkpoint_OLD.sav". Finally a buffer is saved as "checkpoint.sav"
(essentially we are backing up a saved buffer file each time we save it,
so that there is always a "current" save and an "old" save file).
