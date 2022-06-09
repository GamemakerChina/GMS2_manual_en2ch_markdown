# date_leap_year

This function will return true if the year component of the given
datetime value is a leap year or false otherwise. This can be a handy
function for things like Easter Eggs in your games, or for unlocking
special content.

#### Syntax:

``` gml
date_leap_year(date);
```

|          |                                                                                                                         |                      |
|----------|-------------------------------------------------------------------------------------------------------------------------|----------------------|
| Argument | Type                                                                                                                    | Description          |
| date     |  [Datetime](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Date_And_Time/date_current_datetime)  | The datetime to use. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if date_leap_year(date_current_datetime())
{
    if !global.ExtraContent
    {
        global.ExtraContent = true;
    }
}
```

The above code will check the current datetime to see if the year is a
leap year or not. If it is it sets a global variable.
