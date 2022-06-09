# Random Action Library

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Random/Lib_Mathematics.png)  
The **Random** library has the following actions for dealing with random
number generation and chance operations:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Random/i_Mathematics_Get_Random_Number.png" /><br />
</td>
<td><a href="Get_Random_Number">Get Random Number</a></td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Random/i_Mathematics_Randomise.png" /><br />
</td>
<td><a href="Randomise">Randomise</a></td>
</tr>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Random/i_Mathematics_Choose.png" /><br />
</td>
<td><a href="Choose">Choose</a></td>
</tr>
</tbody>
</table>

It is worth noting that GameMaker will use the same seed when generating
random numbers each time you run the game from the IDE. This is to
facilitate debugging and means that you will get the same initial
results when generating random values, but this will *not* occur when
you have compiled the game into an executable (a new seed will be
generated each time the game is run). If you do not wish this behaviour
when testing, then you should call the [Randomise](Randomise) action
once at the start of the game, before generating any random values.
