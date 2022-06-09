# os_get_language

This function returns a string with the two letter Language Code for the
OS that is running the game, as set by the
[ISO639](http://en.wikipedia.org/wiki/ISO_639) standard. If the
information is not available, it will hold simply an empty string "", or
"en" for "English" language. Note that some languages also have a
relevant Regional Code too, so to distinguish between different regions
of the same country use the function [ os_get_region()
](os_get_region) . The following table shows example of some of the
main two letter language codes as defined by ISO 639:

|            |      |
|------------|------|
| Language   | Code |
| Arabic     | ar   |
| Chinese    | zh   |
| Danish     | da   |
| English    | en   |
| French     | fr   |
| German     | de   |
| Greek      | el   |
| Italian    | it   |
| Japanese   | ja   |
| Norwegian  | no   |
| Polish     | pl   |
| Portuguese | pt   |
| Russian    | ru   |
| Spanish    | es   |
| Swedish    | sv   |

**NOTE** : This is not the location country code that is returned, but
the language code of the OS.

#### Syntax:

``` gml
os_get_language()
```

#### Returns:

``` gml
 String
```

#### Example:

``` gml
switch (os_get_language())
{
    case "es": ini_open("spanish.ini"); break;
    case "fr": ini_open("french.ini"); break;
    case "it": ini_open("italian.ini"); break;
    default: ini_open("english.ini"); break;
}
```

The above code checks the OS language and opens a different \*.ini file
depending on the returned value.
