# Object Variables

When you click on the **Variables** button it will open up the **Object
Variables** window, which you can then use to generate any number of
variables *before* the Create Event of the object:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Object_Variables.png)  
In this window you can click on the button **Add** to add a new
variable to the list. You can then **name** the variable as well as set
its **type** and adjust its **properties** :  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Object_NewVariable.png)  
The variable name must start with a letter and can contain only letters,
numbers, and the underscore symbol '\_' with a maximum length of 64
symbols. So, valid variables are things like fish , foo_bar , num1 , and
*invalid* variables would be 6fish , foo bar , or \*num . Once you have
given the name of the variable you need to set its type, which can be
any of the following:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Object_VariableTypes.png)  
It is worth noting that this feature is particularly useful when working
with parent/child instances - since you can have a parent object with a
set of defined variables and then simply modify them in child object
(see the section **Object Variables And Child Objects** below for more
details) - and for when you add instances into the [Room
Editor](../Rooms) (see the section on **Layers** \> **Instance
Layer** ), since you can also modify these variables for individual
instances that have been placed in the room. The different types of
variable that you can create are listed below:

-   **Real** : A real number is any number that is not a whole integer
    and can be positive or negative. So, 124.5 , 45639.566546456 , 0.9 ,
    -45.5 etc... are all examples of real numbers. All real numbers are
    stored as 64bit floating point values (doubles). The **real** (and
    **integer** ) data types have an option for setting a range of
    values which can be accessed by clicking the **Options**  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_VariableOptions.png)  
    button:  
    ![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Object_RealOptions.png)  
    When you check this you can then input a start value and an end
    value and instead of having a fixed value shown for the variable in
    the Object Variables window, you will have a slider that is clamped
    to these values:  
    ![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Object_VariableRange.png)  
-   **Integer** : An integer is a whole number and can be positive or
    negative, for example 30004 , 19 , 0 , -300 . Note that you can set
    a range of values for the output integer, as explained above for
    real numbers.
-   **String** : A string is anything that has been placed within double
    quotation marks, for example "fish", "Hello World", or "12345".
-   **Boolean** : A boolean is a value that is either true or false. In
    the Object Editor Variables window, this is simply shown as a box
    that you check for true and uncheck for false.
-   **Expression** : An expression is a mathematical phrase that can
    contain ordinary numbers, variables, strings, or GML functions as
    well as one or more operators. For example sqrt(85 \* 6) + 5.5 is an
    expression.
-   **Resource** : A resource is simply any one of the resources that
    you have defined in the Asset Browser. When you select this resource
    type, you can then click on the **Open Asset Explorer**  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_OpenAssetExplorer.png)  
    button to open the Asset Explorer and select the resource you
    require.
-   **List** : Selecting a list type of input means that you can then
    create a selection of values (these can be strings, reals,
    expressions etc...) of which you can then choose one or more for the
    variable to return. To define the items that go in the list you need
    to add them into the **Options** first (click the  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_VariableOptions.png)  
    button):  
    ![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Object_ListOptions.png)  
    You will be able to choose the item as the default value for the
    variable in the main window from the drop down menu:  
    ![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Object_ListType.png)  
    Note that if you have **Multi-select** ticked in the List Options
    then the variable will become an array of all the selected
    options:  
    ![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Object_ListArray.png)  
-   **Colour** : The colour type is for you to define a colour value to
    be stored in the variable. You can input a real number (from 0 to
    16777216, this will have an alpha value of 255), or a hex value (in
    the format of $RRGGBBAA), or you can double click  
    ![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_LMB.png)  
    on the colour swatch to open the **Colour Picker** and define the
    colour there.

# Object Variables And Child Objects

An important feature of the Object Variables is that they are
*inherited* by any child objects that you have in the Asset Browser (see
the section on [Parent Objects](Parent_Objects) for more
information), which means that you can then choose to override or change
any or all of them if you wish. When you create a child object of
another object resource that has Variables defined for it, these will
show up in the Object Variables window like this:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Object_ChildVariables.png)  
You can see in the top image that the Parent object has four Object
Variables and in the bottom image these are also shown, only "greyed
out" and have the **Inherited From Parent**  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_InheritedVariable.png)  
icon to indicate that they have been inherited. These inherited
variables can then be edited if you click the **Override Variable**  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_OverrideVariable.png)  
button, so you can then adjust the range slider or values, or select
different items from lists, etc... Note that when you edit a parent
variable *you can only change the defined value* but not the name, nor
can you change the variable options. Also note that you can add in new
Object Variables to child objects as well (and in the example image
above you can see that "Character Type" is a new Object Variable only
for the child object). If you have edited an inherited Object Variable,
then you can click the Delete  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_DeleteVariable.png)  
button to remove the edit, but not the variable. The variable will still
be inherited from the parent, but will use the parent default value
again. If you need to completely remove the variable, then you must do
this from the parent object.
