# ImportJSON

Import JSON directly into Google Sheets. To use go to `Tools` > `Script Editor` and add the script and save.

The main function available is **ImportJSON**. To use it pass it a URL along with an XPath query selector and an options comma separated value.

    =ImportJSON("http://example.com/page.json", "/page/entry/title,/page/entry/content", "noInherit,noTruncate,rawHeaders")

Options are
* **noInherit** - Don't inherit values from parent elements
* **noTruncate** - Don't truncate values
* **rawHeaders** - Don't prettify headers
* **noHeaders** - Don't include headers, only the data
* **debugLocation** - Prepend each value with the row & column it belongs in


The JSON feed is flattened to create a two-dimensional array. The first row contains the headers, with each column header indicating the path to that data in the JSON feed. The remaining rows contain the data. 

Review **ImportJSON.gs** for full documentation.

## Changelog

- v1.2.1 - Fixed a bug with how nested arrays are handled. The rowIndex counter wasn't incrementing properly when parsing.
- v1.2.0 - Added ImportJSONViaPost and support for fetchOptions to ImportJSONAdvanced
- v1.1.1 - Added a version number using Google Scripts Versioning so other developers can use the library
- v1.1.0 - Added support for the noHeaders option
- v1.0.0 - Initial release

## Author

- Brad Jasper
- Trevor Lohrbeer (up to v1.2.1)

