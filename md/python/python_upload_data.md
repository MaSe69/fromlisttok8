---
layout: page_public
title: List to K8s
meta: Overview Meta
permalink: /python_upload_data/
---

# Upload your data

Your data source should be a csv file. See here for details on [Data Input](../data_input).

Your csv-file that contains your list should have the first row as header, i.e. only 1 row and no row in that file before the header. 
Starting with row 2, the body of your list starts.


## Python support for csv-Files

Python offers a convenient module to import from a csv-file.

<code>
import csv
...
with open(filename) as csv_file:
csv_reader = csv.reader(csv_file, delimiter=";")
    for row in csv_reader:
<code>

Once the file is 







