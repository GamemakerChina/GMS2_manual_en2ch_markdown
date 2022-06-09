# Files Action Library

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/Lib_Files.png)  
The **File Actions** deal with two different file types - Buffer files
and Ini files - and also have certain generic file actions to rename or
copy existing files. **Buffer files** are created by saving out the data
from a buffer that you have previously created and this data can then be
loaded into a buffer again at any time in the future. You can find out
more information about buffers here: [Buffer
Actions](../Buffers/Buffer_Actions) . **Ini files** are small,
lightweight files which are compatible with most platforms. They are
ideal for storing small pieces of information, like interface
preferences, local high scores, level data etc... and are very easy to
use. Ini files don't have to have been created previously to use these
actions, and you can read from a non-existent Ini file and you'll simply
get a default return value (which you specify), however we recommend
that you create at least a "base" ini file for opening and modifying
before using the actions. This base ini file can be created by simply
calling the <a href="Open_Ini_File" data-a="">Open Ini File</a>
action followed by the [Close Ini File](Close_Ini_File) , since
closing the file will write it to the disk, or you can include one in
the [Included Files](../../../Settings/Included_Files) of the Asset
Browser. If you are using a file included in the Asset Browser as your
base Ini, you should also read the section of the manual about [how the
File System works](../../../Additional_Information/The_File_System)
. **NOTE** : For games with localizations it is very important that
accented letters can be read from external files. This means that you
should create the ini file in **UTF8 format** first and then add it into
GameMaker as an included file so that it is exported on running the game
and used instead of the default ANSI format ini file that is created by
the ini functions when none has been previously supplied. In this way,
you can read and write to it correctly with all accents and non-roman
letters being maintained. The following actions exist for working with
files:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/i_Files_Load_Buffer.png" /><br />
</td>
<td><a href="Load_Buffer">Load Buffer</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/i_Files_Save_Buffer.png" /><br />
</td>
<td><a href="Save_Buffer">Save Buffer</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/i_Files_Rename_File.png" /><br />
</td>
<td><a href="Rename_File">Rename File</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/i_Files_Copy_File.png" /><br />
</td>
<td><a href="Copy_File">Copy File</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/i_Files_Delete_File.png" /><br />
</td>
<td><a href="Delete_File">Delete File</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/i_Files_Open_Ini_File.png" /><br />
</td>
<td><a href="Open_Ini_File">Open Ini File</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/i_Files_Close_Ini_File.png" /><br />
</td>
<td><a href="Close_Ini_File">Close Ini File</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/i_Files_Write_To_Ini_File.png" /><br />
</td>
<td><a href="Write_To_Ini_File">Write To Ini File</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/i_Files_Read_Ini_File.png" /><br />
</td>
<td><a href="Read_Ini_File">Read Ini File</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Files/i_Files_If_File_Exists.png" /><br />
</td>
<td><a href="If_File_Exists">If File Exists</a></td>
</tr>
</tbody>
</table>
