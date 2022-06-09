# clipboard_has_text

This function will return true if the clipboard contains text or false
if it does not. NOTE This function is only valid on the Windows, HTML5
and Opera GX targets. On HTML5, clipboards are [not supported on
Firefox](https://developer.mozilla.org/en-US/docs/Web/API/Clipboard#browser_compatibility)
without the use of an extension, and are not supported on Internet
Explorer at all.

#### Syntax:

``` gml
clipboard_has_text();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if clipboard_has_text()
{
    str = clipboard_get_text();
    clipboard_set_text("");
}
```

The above code checks the clipboard for text and if it contains any, it
is read as a string into the variable "str". Finally the clipboard is
cleared by setting it to an empty string.
