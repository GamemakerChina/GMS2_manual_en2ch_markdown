# Binary Files

In rare situations you might need to read data from binary files. These
functions can be used for that purpose, although in general, we'd
recommend that you use the dedicated [buffer
functions](../../Buffers/Buffers) to create, save and load binary
data rather than these functions. **NOTE** : These functions **do not**
work when the target module is HTML5. The following low-level routines
exist for this:

-   [file_bin_open](file_bin_open)
-   [file_bin_rewrite](file_bin_rewrite)
-   [file_bin_close](file_bin_close)
-   [file_bin_size](file_bin_size)
-   [file_bin_position](file_bin_position)
-   [file_bin_seek](file_bin_seek)
-   [file_bin_write_byte](file_bin_write_byte)
-   [file_bin_read_byte](file_bin_read_byte)
