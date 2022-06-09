#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Loops/i_Loops_Break.png) Break

This action can only be used within a loop action (for example,
[Repeat](Repeat) or [While](While) ), and calling it will break
out of the loop in that moment. Normally a loop will run either a fixed
number of times or until a specific condition is met, but you can use
the Break action to prematurely end a loop at any moment (actions within
the loop *after* the Break will not be run).

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Loops/a_Loops_Break.png)  

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Loops/e_Loops_Break.png)  
The above action block code performs a Repeat loop 1000 times. In the
loop it checks to see if a List data structure is empty and if it is
*not* it removes an item from the list, and if it *is* it breaks the
loop.
