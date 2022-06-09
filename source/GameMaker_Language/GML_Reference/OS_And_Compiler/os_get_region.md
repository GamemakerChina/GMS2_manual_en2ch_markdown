# os_get_region

This function returns a string with the two or three letter Regional
Code for the OS that is running the game, as set by the
[ISO3166-1](http://en.wikipedia.org/wiki/ISO_3166-1) standard. If the
information is not available, it will hold simply an empty string "".
**NOTE** : This is not the location regional code that is returned, but
the regional language code of the OS.

#### Syntax:

``` gml
os_get_region()
```

#### Returns:

``` gml
 String
```

#### Example:

``` gml
switch (os_get_language())
{
    case "zh":
        var region = os_get_region();
        if (region == "HK" || region == "MO" || region == "TW")
        {
            ini_open("chinese_traditional.ini");
        }
        else
        {
            ini_open("chinese_simplified.ini");
        }
    break;

    case "fr":
        ini_open("french.ini");
    break;

    case "it":
        ini_open("italian.ini");
    break;

    default:
        ini_open("english.ini");
    break;
}
```

The above code checks the OS language and if it is Chinese, it then
checks the OS region, opening a different \*.ini file depending on the
returned values.
