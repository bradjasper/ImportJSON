# ImportJSON

Add an =ImportJSON() function to Google Sheets, allowing quick and easy JSON importing. To use go to `Tools` > `Script Editor` and add the `ImportJSON.gs` file. Now in your spreadsheet you can access the `ImportJSON()` function. Use it like this:

    =ImportJSON("https://mysafeinfo.com/api/data?list=bestnovels&format=json&rows=20&alias=cnt=count,avg=average_rank,tt=title,au=author,yr=year", "/title")

Here are all of the functions included

     `ImportJSON`            For use by end users to import a JSON feed from a URL 
     `ImportJSONFromSheet`   For use by end users to import JSON from one of the Sheets
     `ImportJSONViaPost`     For use by end users to import a JSON feed from a URL using POST parameters
     `ImportJSONAdvanced`    For use by script developers to easily extend the functionality of this library
     `ImportJSONBasicAuth`   For use by end users to import a JSON feed from a URL with HTTP Basic Auth (added by Karsten Lettow)

Review `ImportJSON.gs` for more info on how to use these in detail.

## Version
- 1.4.0 (July 23, 2017) - Transfer project to Brad Jasper. Fixed off-by-one array bug. Fixed previous value bug. Added custom annotations. Added ImportJSONFromSheet and ImportJSONBasicAuth.
- 1.3.0 - Adds ability to import the text from a set of rows containing the text to parse. All cells are concatenated
- 1.2.1 - Fixed a bug with how nested arrays are handled. The rowIndex counter wasn't incrementing properly when parsing.
- 1.2.0 - Added ImportJSONViaPost and support for fetchOptions to ImportJSONAdvanced
- 1.1.1 - Added a version number using Google Scripts Versioning so other developers can use the library
- 1.1.0 - Added support for the noHeaders option
- 1.0.0 - Initial release

## How can you help?
- Found a bug? Report it! https://github.com/bradjasper/ImportJSON/issues
- Want to contribute? Submit an <a href="https://github.com/bradjasper/ImportJSON/issues?q=is%3Aissue+is%3Aopen+label%3Aenhancement">enhancement</a>

## Author
- Brad Jasper (v1.4.0 and beyond)
- Trevor Lohrbeer (up to v1.4.0)

## Website archive
This code base used to be hosted at http://blog.fastfedora.com/projects/import-json and contained a lot of useful information. It has been archived at https://rawgit.com/bradjasper/ImportJSON/master/archive/blog.fastfedora.com/projects/import-json.html

