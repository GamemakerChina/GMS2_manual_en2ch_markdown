# Encoding And Hashing

When dealing with external files, there is always the possibility that
the end user could open and change the information that they contain,
and so change your game. This can result in broken game-play elements or
fraudulent scores on-line (for example), and so GameMaker provides you
with some basic encoding functions as well as functions to perform
hashing checks on strings and files to make sure that they have
maintained their integrity before being used. There are also some
functions supplied for encoding and decoding JSON format strings. **
NOTE ** Encoding is NOT encryption! A base64 encoding renders the file
unreadable to the naked eye and will require an effort on behalf of the
user to decode, but it is not secure from hacking. It is recommended
that you mix those functions with your own encryption (there are many
forms of encryption and script functions for GameMaker are available on
the internet).

-   [json_encode](json_encode)
-   [json_decode](json_decode)
-   [json_stringify](json_stringify)
-   [json_parse](json_parse)
-   [base64_encode](base64_encode)
-   [base64_decode](base64_decode)
-   [md5_string_utf8](md5_string_utf8)
-   [md5_string_unicode](md5_string_unicode)
-   [md5_file](md5_file)
-   [sha1_string_utf8](sha1_string_utf8)
-   [sha1_string_unicode](sha1_string_unicode)
-   [sha1_file](sha1_file)
-   [zip_unzip](zip_unzip)
-   [load_csv](load_csv)

It is worth noting that there are also a number of functions related to
encoding and hashing [Buffers](../../Buffers/Buffers) , which you
can find from the following links:

-   [buffer_md5](../../Buffers/buffer_md5)
-   [buffer_sha1](../../Buffers/buffer_sha1)
-   [buffer_crc32](../../Buffers/buffer_crc32)
-   [buffer_base64_encode](../../Buffers/buffer_base64_encode)
-   [buffer_base64_decode](../../Buffers/buffer_base64_decode)
-   [buffer_base64_decode_ext](../../Buffers/buffer_base64_decode_ext)
