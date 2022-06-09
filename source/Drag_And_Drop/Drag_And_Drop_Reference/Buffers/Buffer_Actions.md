# Buffers Action Library

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Buffers/Lib_Buffers.png)  
A **buffer** is a region of physical memory used to temporarily hold
data while it is being moved from one place to another or manipulated in
some way, for example you can use a buffer to hold game state data.
GameMaker has a number of specific actions related to creating,
modifying and loading/saving buffers, but before using them please note
the following points:

-   When a buffer is created, it is automatically cleared and filled to
    0.
-   The "size" argument of the buffer functions always refers to the
    size *in bytes* of the buffer.
-   GML Visual buffers are always *1 byte aligned* . The "alignment"
    refers to how data is stored within a buffer and is used when using
    the [GML buffer
    Functions](../../../GameMaker_Language/GML_Reference/Buffers/Buffers)
    , but for GML Visual , it's not relevant.
-   Data in buffers is read and written in a *sequential* manner (ie:
    you call the [Write Buffer](Write_Buffer) action three times,
    then it will write the first data, move forward, right the second
    data, move forward and then write the last data), with something
    called the "seek" value to tell you where in the buffer the next
    read/write will take place.
-   All data is written to the buffer and returned from the buffer as a
    **string** so if you have stored any real numbers you will have to
    use one of the [Data Type
    Actions](../Data_Types/Data_Type_Actions) to convert it from the
    string to the value.

The memory used for creating buffers is system memory so even when the
game doesn't have focus, any data stored in a buffer should be safe,
however if the app is closed or re-started then it will be lost. It is
also worth noting that buffers can also be saved as files then loaded
back into the game using the [file actions](../Files/File_Actions) .
The following page explains in more detail how buffers work within the
context of GameMaker and contain a couple of GML code examples:

-   [Using
    Buffers](../../../Additional_Information/Guide_To_Using_Buffers)

The **Buffer** library has the following actions:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Buffers/i_Buffers_Create_Buffer.png" /><br />
</td>
<td><a href="Create_Buffer">Create Buffer</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Buffers/i_Buffers_Copy_Buffer.png" /><br />
</td>
<td><a href="Copy_Buffer">Copy Buffer</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Buffers/i_Buffers_Delete_Buffer.png" /><br />
</td>
<td><a href="Delete_Buffer">Delete Buffer</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Buffers/i_Buffers_Read_Buffer.png" /><br />
</td>
<td><a href="Read_Buffer">Read Buffer</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Buffers/i_Buffers_Write_Buffer.png" /><br />
</td>
<td><a href="Write_Buffer">Write Buffer</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Buffers/i_Buffers_Seek_Buffer.png" /><br />
</td>
<td><a href="Seek_Buffer">Seek Buffer</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Buffers/i_Buffers_Get_Buffer_Size.png" /><br />
</td>
<td><a href="Get_Buffer_Size">Get Buffer Size</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Buffers/i_Buffers_Get_Buffer_Position.png" /><br />
</td>
<td><a href="Get_Buffer_Position">Get Buffer Position</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Buffers/i_Buffers_If_Buffer_Exists.png" /><br />
</td>
<td><a href="If_Buffer_Exists">If Buffer Exists</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Buffers/i_Buffers_If_End_Of_Buffer.png" /><br />
</td>
<td><a href="If_End_Of_Buffer">If End Of Buffer</a></td>
</tr>
</tbody>
</table>
