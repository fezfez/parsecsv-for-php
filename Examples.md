### General: ###
```
$csv = new parseCSV('data.csv');
print_r($csv->data);
```


### Tab delimited, and encoding conversion: ###
```
$csv = new parseCSV();
$csv->encoding('UTF-16', 'UTF-8');
$csv->delimiter = "\t";
$csv->parse('data.tsv');
print_r($csv->data);
```


### Auto-detect delimiter character: ###
```
$csv = new parseCSV();
$csv->auto('data.csv');
print_r($csv->data);
```


###  ###
### Modify data in a CSV file: ###
```
$csv = new parseCSV();
$csv->sort_by = 'id';
$csv->parse('data.csv');
# "4" is the value of the "id" column of the CSV row
$csv->data[4] = array('firstname' => 'John', 'lastname' => 'Doe', 'email' => 'john@doe.com');
$csv->save();
```


### Add row/entry to end of CSV file: ###
_Only recommended when you know the extact sctructure of the file._
```
$csv = new parseCSV();
$csv->save('data.csv', array('1986', 'Home', 'Nowhere', ''), true);
```


### Convert 2D array to csv data and send headers to browser to treat output as a file and download it: ###
```
$csv = new parseCSV();
$csv->output (true, 'movies.csv', $array);
```

