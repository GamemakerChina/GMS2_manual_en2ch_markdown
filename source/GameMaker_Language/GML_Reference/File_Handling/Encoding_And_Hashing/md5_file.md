# md5_file

In cryptography, MD5 (Message-Digest algorithm 5) is a widely used
cryptographic hash function with a 128-bit hash value and has been
employed in a wide variety of security applications. It is also commonly
used to check the integrity of files and strings. This function will
take the given file and generate a unique MD5 for that file which can
then be stored for later use. **NOTE** : MD5 is not completely secure
and can be broken. See [this page](https://en.wikipedia.org/wiki/MD5)
for more info.

#### Syntax:

``` gml
md5_file(filename)
```

|          |                                                                           |                                        |
|----------|---------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                      | Description                            |
| filename |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The file to generate the MD5 hash for. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
hash = md5_file(working_directory + "game_data.ini")
```

The above code will generate an MD5 hash for the specified file and
store the returned value in the variable "hash".
