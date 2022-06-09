# sha1_file

In cryptography, SHA-1 is a cryptographic hash function designed by the
United States *National Security Agency* and is employed in several
widely used applications popular **Git** where it is used to check for
file changes, and the protocols TLS and SSL, PGP, SSH, S/MIME, and
IPsec. This function will take an input file and return a 160 bit
message digest in ASCII format unique to that file to be used for
integrity verification at any later date. **NOTE** : SHA-1 is not
completely secure and can be broken. See [this
page](https://en.wikipedia.org/wiki/SHA-1) for more info.

#### Syntax:

``` gml
sha1_file(filename)
```

|          |                                                                           |                                         |
|----------|---------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                      | Description                             |
| filename |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The file to generate the sha1 hash for. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
hash = sha1_file(working_directory + "game_data.ini")
```

The above code will generate a sha1 hash for the specified file and
store the returned value in the variable "hash".
