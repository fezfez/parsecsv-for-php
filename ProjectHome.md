## This project has been moved to Github: ##
https://github.com/parsecsv/parsecsv-for-php


---


_**parseCSV**_ is an easy to use PHP class to read and write CSV data properly. It fully conforms to the specifications outlined on the on the [Wikipedia article](http://en.wikipedia.org/wiki/Comma-separated_values). It has a few advanced features which help make your life easier when dealing with CSV data.

I created this class due to the lack of built-in and third-party support for handling CSV data in PHP.

Please check the [Examples](http://code.google.com/p/parsecsv-for-php/wiki/Examples) page for basic sample code illustrating the use of parseCSV.


### Features: ###
  * parseCSV is the only complete and fully featured CSV solution for PHP (as far as i know).
  * Supports enclosed values, enclosed commas, double quotes and new lines.
  * Automatic delimiter character detection.
  * Sort data by specific fields/columns.
  * Easy data manipulation.
  * Basic SQL-like _conditions_, _offset_ and _limit_ options for filtering data.
  * Error detection for incorrectly formatted input. It attempts to be intelligent, but can not be trusted 100% due to the structure of CSV, and how different programs like Excel for example outputs CSV data.
  * Support for character encoding conversion using PHP's _iconv_ function (requires PHP 5).
  * Supports both PHP 4 & 5.


### Planned Features: ###
  * Support negative _offset_ values to offset from end of data rather than beginning.
  * More advanced and mature conditions input. Currently it doesn't even support enclosing values in quotes.
  * Some decent documentation, specifically regarding _conditions_ syntax.


### Credits: ###
  * parseCSV is based on the concept of [Ming Hong Ng](http://minghong.blogspot.com/)'s [CsvFileParser](http://minghong.blogspot.com/2006/07/csv-parser-for-php.html) class.


### Contact: ###
If you have any problems, questions or suggestions please create a new [issue](http://code.google.com/p/parsecsv-for-php/issues/list), or feel free to drop me a mail: contact at jimeh dot me