#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/i_Files_Copy_File.png) Copy File

With this action you can copy any file that has been saved by your game
or has been bundled as part of the Included Files. You give the name of
the file to copy (as a string) and then the name of the file to create
as a copy of the original file (also as a string and including the file
extension). The given file will be duplicated and given the new name.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/a_Files_Copy_File.png)  

#### Arguments:

|          |                                                            |
|----------|------------------------------------------------------------|
| Argument | Description                                                |
| Filename | The name (as a string) of the file to copy                 |
| Copy To  | The name (as a string) of the file to be created as a copy |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/e_Files_Copy_File.png)  
The above action block code will check to see if an ini file does *not*
exists and if it does not then it is created by copying another file.
