# The Script Editor

  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Scripts.png)  
This section deals with the **script editor** (also called the **text
editor** ) which is where you type in all the code that your game will
require to run. This editor is used for creating custom script assets,
as well as for coding [object
events](Object_Properties/Object_Events) , for adding [room creation
code](Room_Properties/Room_Properties) , and for many other things.
This section simply details how the script **editor** works, and *not*
how to create script assets nor how to use GML Code or GML Visual to
make scripts. For that please see the following sections:

-   [GML Code
    Scripts](../GameMaker_Language/GML_Overview/Script_Functions)
-   [GML Visual
    Scripts](../Drag_And_Drop/Drag_And_Drop_Overview/Action_Block_Functions)

On creating a script asset, you may be asked to choose between GML
Visual and GML Code . See [GameMaker
Language](../GameMaker_Language) for more information. The script
editor is where you write your GameMaker Language code, which is the
built-in programming language that GameMaker uses (see the [GameMaker
Language](../GameMaker_Language) section for more details). Once you
become more familiar with GameMaker and want to use it to its fullest
extent, it is advisable to start learning to use this language, as it
greatly expands your possibilities when creating games. A script asset
can be renamed by right-clicking  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RMB.png)  
on it in the [Asset Browser](../Introduction/The_Asset_Browser) and
selecting *Rename* , but note that the script name must conform to the
scripting rules for assets, so they can only be alpha-numeric, must
start with a letter, and the only symbol they can contain is the "\_"
under-bar symbol. The script editor in other places cannot be renamed
and will have a name specific to what is being edited, like an object
event for example. When you open the script editor window it will have
the following options and layout: [ Script / Event Tab Script / Event
Tab ](#) The script editor opens in a window with tabs across the top to
let you have multiple scripts or events in one window (although this
behaviour can be changed from the
[Preferences](../Setting_Up_And_Version_Information/IDE_Preferences/Text_Editor_Preferences)
to give a new window to each script or event). You can click  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
on a tab and then drag it to change the tab order, or - if you prefer
- you can pull it out of the current window and place it on the
workspace to create a new window for that script (or add it to a
different window), and you can also maximise the script editor to create
a new workspace too. If you drag a script tab out of the IDE window,
then a new IDE will be spawned to hold this script resource, and it can
be used as you would the Main window. Note that if you are editing code
from an **object event** in the script editor and you have maximised the
script editor or have it on a separate window or workspace, then the
right-click  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RMB.png)  
editor menu will have some extra options:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Scripts_RMB_Object_Menu.png)  

-   **Restore to workspace** : This will take the script editor out of a
    maximised/workspace state and re-chain it to the object in the
    workspace.
-   **Go to Object** : This will take you to the workspace that the
    object with the code is on and focus on the object.
-   **Add /Open Event** : This permits you to add a new event to the
    object the current script belongs to, and will open a new code tab
    in the Script Editor for the added event. If the event selected
    already has code in it, then this will be opened in a new tab.

For information on the rest of the right-click  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RMB.png)  
menu options, see the section on **Editing** , below. [ Gutter Gutter
](#) The **Gutter** is used to show the line numbers for your code and
also to convey some specific pieces of information about the state of
the code. Most importantly, if you make a typo or construct the code
incorrectly, then the GameMaker IDE will inform you of the issue by
flagging the line of code with a red exclamation mark  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_CodeError.png)  
showing a syntax error. You can then mouse over the symbol to get a
brief description of what the issue is:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Scripts_Errors.png)  
You can find more information on Syntax errors (and general errors when
testing or compiling your code) from the following section:

-   [Error Reporting](../Additional_Information/Error_Reporting)

The gutter will also mark any line of the script that has had a
**breakpoint** added. A breakpoint is simply a place in the script where
you want the [debugger](../IDE_Tools/The_Debugger) to pause the
execution of your game when it is reached. You can toggle a breakpoint
from any line of any script or object event by pressing " f9 " or using
the right-click  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_RMB.png)  
menu. When you add a breakpoint, it will show up like this in the
gutter:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Scripts_Breakpoint.png)  
Finally, the gutter will also show any bookmarked items too. To bookmark
a line of code simply hold down  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
/  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
+  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Shift.png)  
+ Number (from 0 to 9), and this will permit you to skip back to this
line of code from anywhere in the IDE simply by using  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
/  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
+ Number (from 0 to 9). To delete the bookmark, simply perform the same
action as you used to add it on the line of code again. When a bookmark
has been added, it will show like this:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Scripts_Bookmark.png)  
[ Search / Replace Search / Replace ](#) While working in the script
editor, you can press  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
/  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
+ " F " to open up the Search box or  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
/  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
+ " H " to open up Search and Replace:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Scripts_Search.png)  
Here you can perform a *local* search for the keyword you input and once
you have entered your search term, you can then use the arrows at the
top right of the search window to skip from one found term to the next
in the script. You can change how the search operation is carried out by
toggling the following buttons:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_ExactWord.png" /><br />
</td>
<td>When you toggle this, the search function will only highlight those
strings that match the whole input string. For example, with it off a
search for " <em>random</em> " will show up all words that contain this
string - like <span> irandom() </span> , or <span> randomise() </span> -
while toggling it to on would only show the function <span> random()
</span> .</td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_CaseSensitive.png" /><br />
</td>
<td>When this option is toggled, you are telling <span> GameMaker
</span> to check not only the contents of the search string, but the
case too. For example, if you have a sprite called " <span> spr_Dog
</span> " and do a search for " <em>dog</em> " with this toggle
<em>off</em> , then the sprite string will be highlighted, however if
the toggle is <em>on</em> then it won't since " <em>Dog</em> " is no
longer considered the same as " <em>dog</em> ".</td>
</tr>
</tbody>
</table>

If you have opened the search window using  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
/  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
+ " F ", then the replace functionality will not be visible, so you need
to click the Replace button  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_ReplaceToggle.png)  
to open it. Once open, you can then enter a string that will be used to
replace any given search string, using the following buttons to perform
the action:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_ReplaceNext.png" /><br />
</td>
<td>Clicking this will replace the next search string found in the
script with the given replace string. Note that the "next" term is
considered the next one after the current cursor position, and you can
skip to different ones using arrow buttons at the top right of the
search window.</td>
</tr>
<tr class="even">
<td><br />
<img
src="https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_ReplaceAll.png" /><br />
</td>
<td>Clicking this will replace <em>all</em> examples of the search
string within the script using the given replace string.</td>
</tr>
</tbody>
</table>

Note that if you want to do a *global* search (ie: search the whole
project rather than the current script or event), then you can press  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Ctrl.png)  
/  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Cmd.png)  
+  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Shift.png)  
+ "F". [ Main Code Editor Main Code Editor ](#) The main code editor is
where you'll write all your code to create the script asset or fill an
object event. The actual edition of your code is covered in the section
on **Editing** further down this page. [ Information Information ](#)
The information bar at the bottom of the IDE shows you the current line
number you are on and the position along the line. It is also where you
can see the code helper, which is a line of text that shows the function
you are currently editing along with the arguments it requires. As you
fill in the function in the editor, the arguments will highlight to show
you which one you are currently editing. Note that any optional
arguments in your script functions will be shown with \[\] brackets
around them. If you have used the [JSDoc Script
Comments](Code_Editor_Properties/JSDoc_Script_Comments) within a
script asset then the information you have supplied will also show here.
You can get further information about using the script and code editors
from the following pages:

-   [Editing Code](Code_Editor_Properties/Editing_Code)
-   [JSDoc Comments](Code_Editor_Properties/JSDoc_Script_Comments)
-   [Code Snippets](Code_Editor_Properties/Code_Snippets)
