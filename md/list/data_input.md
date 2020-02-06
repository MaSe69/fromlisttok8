---
layout: page_public
title: List to K8s
meta: Overview Meta
permalink: /data_input/
---


# Data Input

Often lists start from scratch in a new Excel sheet. All entries are entered manually.
Obviously, this is only possible for a limited number of data.

In cases of existing or abundant data, you need a data input from other source. These data come in a format. There are currently two major formats
- csv
- json

## Excel Format and Import/Export

Excel tends to make you saving your lists in *.xlsx format. This is fine, if you are sure that your lists never leave the world of Excel. Possibly, that is also what Excel wants you to do - to not leave. However, if you intend to leave, you need another format. 

In Excel, you can save a single sheet as csv, but you cannot use the 'Save Button' to save as JSON.
Data import and export to Excel sheets can be done using either csv or JSON or various other formats.


## CSV (Comma Separated Values)

A most simple list format is to separate the fields by commas.

Example: 
Ingredients unit, quantity
eggs, pieces, 6
butter, gramm, 250

You might wonder what to do, if your fields contain already commas, which is often to case with names: Doe, John. Then, you can replace the coma to separate with an other punctuation mark, commonly the semicolon ";" is used. As it is rare in common values, the vertical line "|" is a good separator, too.

Using csv, you typically create a new list for each list. Recommendably, you do not use csv for trees.


## JSON (JavaScript Object Notation)

JSON is used as the standard format in web services. 
JSON is particularly suited for one-to-many relationships. 
Use JSON for trees.