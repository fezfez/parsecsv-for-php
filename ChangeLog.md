### parseCSV 0.4.3 beta ###
**_Date: 1-July-2008_**
  * Fixed [#4](http://code.google.com/p/parsecsv-for-php/issues/detail?id=4). Added an option for setting sorting type behavior when sorting data. Simply set $csv->sort\_type to "regular", "numeric", or "string".
  * Fixed [#6](http://code.google.com/p/parsecsv-for-php/issues/detail?id=6). Raw loaded file data is now cleared from file\_data property when it has been successfully parsed to keep parseCSV's memory footprint to a minimum. Specifically handy when using mulitple instances of parseCSV to process large files.

### parseCSV 0.4.1 beta ###
**_Date: 31-May-2008_**
  * IMPORTANT! If you're using the output() method, please note that the first parameter has been completely removed as it was technically just useless. Instead, the second parameter (filename) doubles as its replacement. Simply put, if filename is not set or null, the output() method will not output a downloadable file. Please update your existing code when using 0.4.2 and later :)
  * Small fix to the headers sent by the output() method.
  * Added a download example using the output() method to the examples folder.

### parseCSV 0.4.1 beta ###
**_Date: 29-May-2008_**
  * Fixed a small bug in how the output() method handles input data.

### parseCSV 0.4 beta ###
**_Date: 11-Apr-2008_**
  * Error reporting for files/data which is corrupt or has formatting errors like using double quotes in a field without enclosing quotes. Or not escaping double quotes with a second one.
  * parse() method does not require input anymore if the "$object->file" property has been set.

I'm calling this a beta release due to the heavy
modifications to the core parsing logic required
for error reporting to work. I have tested the
new code quite extensively, I'm fairly confident
that it still parses exactly as it always has.

The second reason I'm calling it a beta release
is cause I'm sure the error reporting code will
need more refinements and tweaks to detect more
types of errors, as it's only picking two types
or syntax errors right now. However, it seems
these two are the most common errors that you
would be likely to come across.

### parseCSV 0.3.2 ###
**_Date: 1-Apr-2008_**

This is primarily a bug-fix release for a critical bug which was brought to my attention.

  * Fixed a critical bug in conditions parsing which would generate corrupt matching patterns causing the condition(s) to not work at all in some situations.
  * Fixed a small code error which would cause PHP to generate a invalid offset notice when zero length values were fed into the unparse() method to generate CSV data from an array.

**Notice:** If you have been using the "parsecsv-stable"
branch as an external in any of your projects,
please use the "stable/parsecsv" branch from this
point on as I will eventually remove the former due
to it's stupid naming.

### parseCSV 0.3.1 ###
**_Date: 1-Sep-2007_**
  * Small change to default output settings to conform with RFC 4180 (http://rfc.net/rfc4180.html). Only the LF (line feed) character was used by default to separate rows, rather than CRLF (carriage return & line feed).

### parseCSV 0.3.0 ###
**_Date: 9-Aug-2007_**
  * Changed to the MIT license.
  * Added offset and limit options.
  * Added SQL-like conditions for quickly filtering out entries. Documentation on the condition syntax is forthcoming.
  * Small parsing modification to comply with some recent changes to the specifications outlined on Wikipedia's Comma-separated values article.
  * Minor changes and optimizations, and a few spelling corrections. Oops :)
  * Included more complex code examples in the parseCSV download.

### parseCSV 0.2.1 ###
**_Date: 8-Aug-2007_**
  * Fixed stupid code which caused auto function to not work in some situations.

### parseCSV 0.2.0 beta ###
**_Date: 2-Jan-2007_**
  * Added auto() function to automatically detect delimiter character. Useful for user upload incase delimiter is comma (,), tab, or semi-colon (;). Some versions of MS Excel for Windows use semi-colons instead of commas when saving to CSV files. It uses a process of elimination to eliminate characters that can not be the delimiter, so it should work on all CSV-structured files almost no matter what the delimiter is.
  * Generally updated some of the core workings to increase performance, and offer better support for large (1MB and up) files.
  * Added code examples to header comment.

### parseCSV 0.1.6 beta ###
**_Date: 22-Dec-2006_**
  * Updated output() function.

### parseCSV 0.1.5 beta ###
**_Date: 22-Dec-2006_**
  * Added output() function for easy output to browser, for downloading features for example.

### parseCSV 0.1.4 beta ###
**_Date: 17-Dec-2006_**
  * Minor changes and fixes

### parseCSV 0.1.3 beta ###
**_Date: 17-Dec-2006_**
  * Added GPL v2.0 license.

### parseCSV 0.1.2 beta ###
**_Date: 17-Dec-2006_**
  * Added encoding() function for easier character encoding configuration.

### parseCSV 0.1.1 beta ###
**_Date: 24-Nov-2006_**
  * Added support for a PHP die command on first line of csv files if they have a .php extension to protect secure data from being displayed directly to the browser.

### parseCSV 0.1 beta ###
**_Date: 23-Nov-2006_**
  * Initial release.