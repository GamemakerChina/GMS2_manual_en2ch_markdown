# current_time

This **read only** variable will return the number of milliseconds that
have passed since the game was started.

#### Syntax:

``` gml
current_time;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if (current_time &amp;gt; 600000)
{
    msg = show_question_async("Would you like to rate?");
}
```

The above code checks to see if more than 10 minutes have passed before
asking the user a question.
