# xboxlive_get_user_count

With this function you can find the total number of users currently
signed in to the XBox system. The return value will be an integer value,
from 0 - N, where N is the number of signed in users -1.

#### Syntax:

``` gml
xboxlive_get_user_count();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
for(var i = 0; i &amp;lt; xboxlive_get_user_count(); ++i;)
{
    user_id[i] = xboxlive_get_user(i);
}
```

The above loops through all the signed in users and stores their unique
ID pointer in an array.
