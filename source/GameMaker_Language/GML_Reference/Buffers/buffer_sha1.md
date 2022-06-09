# buffer_sha1

In cryptography, SHA-1 is a cryptographic hashing function designed by
the United States National Security Agency and is employed in several
widely used applications and protocols like the popular **Git** where it
is used to check for file changes. This function will take input data
from a buffer and returns a 160 bit message digest in ASCII format. In
this way you can generate a secure key which can be stored and used to
check the integrity of the information being sent to (or received from)
an external server (for example). When applying this to buffers using
this function you must specify the buffer id of the buffer to use, then
an offset value (in bytes) for where to begin, and then a size (again in
bytes) for the region to be hashed. **NOTE** : SHA-1 is not completely
secure and can be broken. See [this
page](https://en.wikipedia.org/wiki/SHA-1) for more info.

#### Syntax:

``` gml
buffer_sha1(buffer, offset, size);
```

|          |                                                                                       |                                 |
|----------|---------------------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                                  | Description                     |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to use. |
| offset   |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The data offset value.          |
| size     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The size of the buffer.         |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
check_string = buffer_sha1(buff, 0, buffer_get_size(buff));
```

The above code will create a sha1 hash for the full data stored in the
buffer indexed by the variable "buff", and store the returned hash in
the variable "check_string".
