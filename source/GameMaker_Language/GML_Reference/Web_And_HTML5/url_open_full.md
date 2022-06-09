# url_open_full

This will open the specified URL on the browser of the chosen target
device, or, if you are using the HTML5 module, in the currently open
browser. The "target" parameter that you specify is the same as the
standard JavaScript "name" value when you use the open() method (be
aware that all but " **\_self** " may result in the browser blocking, or
asking the user if they wish to allow it) and the "options" is the same
as the JavaScript "specs" parameter for controlling what properties the
new window/tab should display (not all browsers may support all
features). Valid targets are:

|          |                                                                                                                                                                                                       |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Target   | Description                                                                                                                                                                                           |
| \_blank  | Opens the linked document in a new window or tab (this will not work if pop-ups are being blocked by the user, in which case you can use the [ clickable\_\* ](Web_And_HTML5) functions instead). |
| \_self   | Opens the linked document in the same frame as it was clicked (this is default).                                                                                                                      |
| \_parent | Opens the linked document in the parent frame.                                                                                                                                                        |
| \_top    | Opens the linked document in the full body of the window.                                                                                                                                             |

Valid options are:

|                                    |                                                                                                                                                        |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Parameters                         | Description                                                                                                                                            |
| **'height=\[** px **\]'**          | The height of the window, with the minimum value being 100.                                                                                            |
| **'width=\[** px **\]'**           | The width of the window, with the minimum value being 100.                                                                                             |
| **'left=\[** px **\]'**            | The left position of the window.                                                                                                                       |
| **'top=\[** px **\]'**             | The top position of the window (IE only).                                                                                                              |
| **'location=\[** boolean **\]'**   | Whether or not to display the address field (default is 1).                                                                                            |
| **'menubar=\[** boolean **\]'**    | Whether or not to display the menu bar (default is 1).                                                                                                 |
| **'resizable=\[** boolean **\]'**  | Whether or not the window is resizable (default is 1).                                                                                                 |
| **'scrollbars=\[** boolean **\]'** | Whether or not to display scroll bars (default is 1).                                                                                                  |
| **'status=\[** boolean **\]'**     | Whether or not to add a status bar (default is 1).                                                                                                     |
| **'titlebar=\[** boolean **\]'**   | Whether or not to display the title bar. This is ignored unless the calling application is an HTML Application or a trusted dialog box (default is 1); |
| **'toolbar=\[** boolean **\]'**    | Whether or not to display the browser toolbar (default is yes).                                                                                        |

NOTE Antivirus software installed on the player's device may cause the
URL to not open, so keep this in mind when using this function.

#### Syntax:

``` gml
url_open_full(url, target, options);
```

|          |                                                                        |                                                               |
|----------|------------------------------------------------------------------------|---------------------------------------------------------------|
| Argument | Type                                                                   | Description                                                   |
| url      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The URL (website address) to link to.                         |
| target   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | This is the target area to open the URL in (see description). |
| options  |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | Standard browser options (see description).                   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
url_open_full("http://yoyogames.com", "_blank", "resizable=0, height=200, scrollbars=0");
```

This would open the YoYo Games homepage in a new window that can't be
resized, has a height of 200 pixels and no scrollbars.
