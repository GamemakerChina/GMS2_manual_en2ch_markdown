# Runner Errors

Even after syntax checking in the code editor and then having the
compiler check your code for [compiler errors](Compiler_Errors) ,
there are still occasions when something can go wrong. In most cases
this will throw a Virtual Machine (VM) runner error (also called a
**runtime exception** ) which looks like this:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Additional_Information/Error_Report.png)  
Runner errors are generally more serious than compile errors as it means
that there is something seriously wrong with your code that neither the
code editor nor the compiler have been able to detect, and as such you
should pay attention to all such errors. When one occurs, you can use
the **Copy** button on the pop-up to copy the error to the clipboard
which you can then paste into a text file (or wherever) for future
reference. The structure of this error is as follows:

-     
    ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Additional_Information/Error_Text_ObjectEvent.png)  
    This shows the Event that the error has occurred in as well as the
    Object (where applicable).
-     
    ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Additional_Information/Error_Text_Information.png)  
    This shows the actual error.  So, it shows the *scope* of the error
    and the type of error it is. The first value in the brackets will be
    the instance ID of the instance that was running the code - or it
    could be one of the special values listed in the table below - and
    the second is an internal value that GameMaker uses for identifying
    bugs and can be ignored. In the case of the image above, it's saying
    that the variable \_image has not been set (ie: does not exist
    before being accessed) on the object obj_EA_DEMO_Control .
-     
    ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Additional_Information/Error_LineNumber.png)  
    This shows the line number that the error occurs on as well as a
    snippet of code showing the position. Note that this is not always
    100% accurate due to the way the game is compiled, but it should be
    enough to help you find exactly where the issue is.

As mentioned above, certain error messages will be identify the scope
not by an instance ID value, but rather by a *negative* value. These
values can be used to pinpoint the exact nature of the error and what it
refers to with the following values possible:

|        |               |
|--------|---------------|
| Prefix | Scope         |
| -1     | Self          |
| -2     | Other         |
| -3     | All           |
| -4     | Noone         |
| -5     | Global        |
| -6     | Not Specified |
| -7     | Local         |

The possible errors from the VM runner are as follows:

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="header">
<th>Error</th>
<th>Message</th>
<th>Operation</th>
<th>Description</th>
</tr>

<tr class="odd">
<td><span> DoSet </span></td>
<td>Invalid comparison type</td>
<td>Data Types</td>
<td>This denotes that the runner has tried to compare two incompatible
data types, like a real number with a string.</td>
</tr>
<tr class="even">
<td><span> DoConv </span></td>
<td>Execution Error</td>
<td>Data Types</td>
<td>This denotes an error in the conversion of one data-type into
another.</td>
</tr>
<tr class="odd">
<td><hr /></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><span> DoAdd </span></td>
<td>Execution Error</td>
<td>Maths</td>
<td>Something has gone wrong when using the addition ( <span> + </span>
) expression.</td>
</tr>
<tr class="odd">
<td><span> DoMul </span></td>
<td>Execution Error</td>
<td>Maths</td>
<td>Something has gone wrong when using the multiplication ( <span> *
</span> ) expression.</td>
</tr>
<tr class="even">
<td><span> DoSub </span></td>
<td>Execution Error</td>
<td>Maths</td>
<td>Something has gone wrong when using the subtraction ( <span> -
</span> ) expression.</td>
</tr>
<tr class="odd">
<td><span> DoSub </span></td>
<td>Execution Engine - Cannot operate on string type</td>
<td>Maths</td>
<td>You are trying to subtract the wrong type of variables (for example
subtract a string from a real).</td>
</tr>
<tr class="even">
<td><span> DoDiv </span></td>
<td>Execution Error</td>
<td>Maths</td>
<td>Something has gone wrong when using the division ( <span> / </span>
or <span> div </span> ) expression.</td>
</tr>
<tr class="odd">
<td><span> DoDiv </span></td>
<td>Execution Engine - Cannot operate on string type</td>
<td>Maths</td>
<td>You are trying to divide the wrong type of variables (for example
divide a string by a real).</td>
</tr>
<tr class="even">
<td><span> DoDiv </span></td>
<td>Divide by zero</td>
<td>Maths</td>
<td>You are attempting to divide by 0 (note this will only happen when
using integer division, dividing a (non-zero) real by 0 will give
infinity as an answer, dividing zero by zero will give NaN as an
answer). You can check for these values with ( <span> is_infinity
</span> ) and ( <span> is_nan </span> )</td>
</tr>
<tr class="odd">
<td><span> DoMod </span></td>
<td>Execution Error</td>
<td>Maths</td>
<td>Something has gone wrong when using the modulo ( <span> mod </span>
) expression.</td>
</tr>
<tr class="even">
<td><span> DoMod </span></td>
<td>Execution Engine - Cannot operate on string type</td>
<td>Maths</td>
<td>You are trying to use modulo ( <span> mod </span> ) on the wrong
type of variables (for example <span> mod </span> a string by a
real).</td>
</tr>
<tr class="odd">
<td><hr /></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><span> DoAnd </span></td>
<td>Execution Error</td>
<td>Bitwise</td>
<td>Something has gone wrong when using the bitwise "and" ( <span> &amp;
</span> ) expression.</td>
</tr>
<tr class="odd">
<td><span> DoAnd </span></td>
<td>Execution Engine - Cannot operate on string type</td>
<td>Bitwise</td>
<td>You are trying to use bitwise "and" ( <span> &amp; </span> ) on the
wrong type of variables (for example trying to "and" a string with a
real).</td>
</tr>
<tr class="even">
<td><span> DoOr </span></td>
<td>Execution Error</td>
<td>Bitwise</td>
<td>Something has gone wrong when using the bitwise "or" ( <span> |
</span> ) expression.</td>
</tr>
<tr class="odd">
<td><span> DoOr </span></td>
<td>Execution Engine - Cannot operate on string type</td>
<td>Bitwise</td>
<td>You are trying to use "or" ( <span> | </span> ) on the wrong type of
variables (for example trying to "or" a string with a real).</td>
</tr>
<tr class="even">
<td><span> DoXor </span></td>
<td>Execution Error</td>
<td>Bitwise</td>
<td>Something has gone wrong when using the bitwise "xor" ( <span> ^
</span> ) expression.</td>
</tr>
<tr class="odd">
<td><span> DoXor </span></td>
<td>Execution Engine - Cannot operate on string type</td>
<td>Bitwise</td>
<td>You are trying to use "xor" ( <span> ^ </span> ) on the wrong type
of variables (for example trying to "xor" a string with a real).</td>
</tr>
<tr class="even">
<td><span> DoShl </span></td>
<td>Execution Error</td>
<td>Bitwise</td>
<td>Something has gone wrong when bitshifting left ( <span> &lt;&lt;
</span> ) a value.</td>
</tr>
<tr class="odd">
<td><span> DoShl </span></td>
<td>Execution Engine - Cannot operate on string type</td>
<td>Bitwise</td>
<td>You are trying to left bitshift ( <span> &lt;&lt; </span> ) the
wrong type of variables (for example trying to bitshift a string).</td>
</tr>
<tr class="even">
<td><span> DoShr </span></td>
<td>Execution Error</td>
<td>Bitwise</td>
<td>Something has gone wrong when bitshifting right ( <span> &gt;&gt;
</span> ) a value.</td>
</tr>
<tr class="odd">
<td><span> DoShr </span></td>
<td>Execution Engine - Cannot operate on string type</td>
<td>Bitwise</td>
<td>You are trying to right bitshift ( <span> &gt;&gt; </span> ) the
wrong type of variables (for example trying to bitshift a string).</td>
</tr>
<tr class="even">
<td><hr /></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><span> DoNeg </span></td>
<td>Execution Error</td>
<td>Negate</td>
<td>You are trying to turn a variable type into a negative when this
type does not permit such an operation.</td>
</tr>
<tr class="even">
<td><span> DoNot </span></td>
<td>Execution Error</td>
<td>Negate</td>
<td>You are trying to "not" a variable type when this type does not
permit such an operation.</td>
</tr>
<tr class="odd">
<td><hr /></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><span> Push </span></td>
<td>Execution Error - Variable Index out of range (var)</td>
<td>Stack</td>
<td>The variable being accessed is out with the established range for
the runner.</td>
</tr>
<tr class="odd">
<td><span> Push </span></td>
<td>Variable Get (var)</td>
<td>Stack</td>
<td>The given variable has not been defined or is unknown.</td>
</tr>
<tr class="even">
<td><span> Pop </span></td>
<td>Variable Index out of range (var)</td>
<td>Stack</td>
<td>The variable being accessed is out with the established range for
the runner.</td>
</tr>
<tr class="odd">
<td><span> Pop </span></td>
<td>Variable Get (var)</td>
<td>Stack</td>
<td>The given variable has not been defined or is unknown.</td>
</tr>
<tr class="even">
<td><hr /></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><span> With </span></td>
<td>Cannot use global in with statement</td>
<td>With</td>
<td>You have tried to use " <span> global </span> " as a variable within
a " <span> with </span> " statement, ie: <span> with (global)    {  
 //do something;    } </span></td>
</tr>
<tr class="even">
<td><span> With </span></td>
<td>Cannot use local in with statement</td>
<td>With</td>
<td>You have tried to use " <span> local </span> " as a variable within
a " <span> with </span> " statement, ie: <span> with (local)    {  
 //do something;    } </span></td>
</tr>
<tr class="odd">
<td><hr /></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><span> DoCall </span></td>
<td>Execution Engine type error</td>
<td>Engine</td>
<td>This is an undefined error within the Virtual Machine. You should
file a bug report should this happen (see: The Help Menu for details on
how to do this.</td>
</tr>
<tr class="odd">
<td><span> Stack Overflow </span></td>
<td>-</td>
<td>Engine</td>
<td>A stack overflow occurs when too much memory is used on the call
stack and when your game attempts to use more space than is available on
the call stack (that is, when it attempts to access memory beyond the
call stack's bounds, which is essentially a buffer overflow), the stack
is said to overflow, resulting in a program crash. Restart your computer
and <span> GameMaker </span> and if the error persists please get in
touch with support and/or file a bug (as explained above).</td>
</tr>
</tbody>
</table>
