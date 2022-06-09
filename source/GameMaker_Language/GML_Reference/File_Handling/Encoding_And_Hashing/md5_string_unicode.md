# md5_string_unicode

In cryptography, MD5 (Message-Digest algorithm 5) is a widely used
cryptographic hash function with a 128-bit hash value and has been
employed in a wide variety of security applications. It is also commonly
used to check the integrity of files and strings. This function will
take an input unicode string (which is 16bits for each char) and return
the 32-character hexadecimal MD5 hash that is unique to that string. In
this way you can generate a secure key which can be stored and used to
check the integrity of the information being sent to (or received from)
an external server (for example). ** NOTE ** There are two formats for
the MD5 encoding, UTF-8 and unicode. Both are provided to facilitate
communication with different server setups, but the most common to use
is unicode. **NOTE** : MD5 is not completely secure and can be broken.
See [this page](https://en.wikipedia.org/wiki/MD5) for more info.

#### Syntax:

``` gml
md5_string_unicode(string)
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
var hash, str; str = base64_encode(game_data); hash = md5_string_unicode(str); http_get("http://www.MacSweeneyGames.com/CatchTheHaggis/gamedata?hash=" + hash); http_get("http://www.MacSweeneyGames.com/CatchTheHaggis/gamedata?data="
+ str);
```

The above code will base64 encode a string and then generate an MD5
hash. Finally, both the hash and the encoded string are sent to a
server.
