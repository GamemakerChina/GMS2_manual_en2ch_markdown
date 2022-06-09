# sha1_string_utf8

In cryptography, SHA-1 is a cryptographic hash function designed by the
United States *National Security Agency* and is employed in several
widely used applications and protocols like the popular **Git** where it
is used to check for file changes. This function will take an input
UTF-8 string (which has a variable number of bytes per character) and
returns a 160 bit message digest in ASCII format, for example:

``` gml
sha1 input string = "The quick brown fox jumps over the lazy dog" sha1 output hash = "2fd4e1c6 7a2d28fc ed849ee1 bb76e739 1b93eb12"
```

In this way you can generate a secure key which can be stored and used
to check the integrity of the information being sent to (or received
from) an external server (for example). **NOTE** : There are two formats
for the sha1 encoding, UTF-8 and unicode. Both are provided to
facilitate communication with different server setups, but the most
common to use is unicode. **NOTE** : SHA-1 is not completely secure and
can be broken. See [this page](https://en.wikipedia.org/wiki/SHA-1) for
more info.

#### Syntax:

``` gml
sha1_string_utf8(string)
```

|          |                                                                           |                     |
|----------|---------------------------------------------------------------------------|---------------------|
| Argument | Type                                                                      | Description         |
| string   |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to hash. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var hash, str; str = json_encode(hiscore_map); hash = sha1_string_utf8(str); ini_open("local.ini");
 ini_write_string("info", "0", hash); ini_close();
 get[0] = http_post_string("http://www.MacSweeney Games.com/CatchTheHaggis?game_hiscores=" + string(global.game_id), str)
```

The above code will encode a DS map into a JSON string. A sha1 hash is
then generated and stored in an ini file so that this can later be used
to check the integrity of the JSON should the same information be
received later form the server. The JSON is then sent.
