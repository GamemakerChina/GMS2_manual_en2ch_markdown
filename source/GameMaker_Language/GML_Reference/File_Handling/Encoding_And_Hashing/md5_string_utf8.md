# md5_string_utf8

In cryptography, MD5 (Message-Digest algorithm 5) is a widely used
cryptographic hash function with a 128-bit hash value and has been
employed in a wide variety of security applications. It is also commonly
used to check the integrity of files and strings. This function will
take an input UTF-8 string (which has a variable number of bytes per
character) and return the 32-character hexadecimal MD5 hash that is
unique to that string. In this way you can generate a secure key which
can be stored and used to check the integrity of the information being
sent to (or received from) an external server (for example). **NOTE** :
There are two formats for the MD5 encoding, UTF-8 and unicode. Both are
provided to facilitate communication with different server setups, but
the most common to use is unicode. **NOTE** : MD5 is not completely
secure and can be broken. See [this
page](https://en.wikipedia.org/wiki/MD5) for more info.

#### Syntax:

``` gml
md5_string_utf8(string)
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
var hash, str; str = json_encode(hiscore_map); hash = md5_string_utf8(str); ini_open("local.ini");
 ini_write_string("info", "0", hash); ini_close();
 get[0] = http_post_string("http://www.MacSweeney Games.com/CatchTheHaggis?game_hiscores=" + string(global.game_id), str)
```

The above code will encode a DS map into a JSON string. An MD5 hash is
then generated and stored in an ini file so that this can later be used
to check the integrity of the JSON should the same information be
received later form the server. The JSON is then sent.
