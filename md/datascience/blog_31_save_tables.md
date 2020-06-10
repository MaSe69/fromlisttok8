---
layout: page_public
title: From Lists to K8s
meta: Overview Meta
permalink: /save_tables/
---

# Save Tables

Previously, we created some tables. Now it is time to save them.

We only save to the file system. A database is not needed at this stage. Much further down the road there comes a point in time when adding functionality would become equal to rewriting a database. Then, it is worth considering to use an existing database.

Here we handle, for a table in dataframe format

- Write to a csv-file
- Read from a csv-file
- Write as a Excel
- Read from Excel

As we need to save to a folder, we should get the absolute path of that folder.
Python returns to us the current path, which is shall be called "stem" here. Using this stem, we don't have to worry in which programming environment we are.

**Coding**
>
    para["Stem"] = os.getcwd()

Based on this stem, we can define a path relative in our programming environment.
Finally, we need a filename. The filename itself can be separated into a "basename" and an "extension". The extenion varies here depending, if we want to write to a csv-file or to an Excel.



## Step 1: Save to a CSV-File

Choosing the separator is one of the freedoms we have on the csv-format. Working with comma and points on currencies, it is more advisable to work with a different separator, e.g. the semicolon ";".

**Coding**
>
    para["Path"] = "/Blog_Data/"
    para["Basename"] = "Accounts"
    para["Delimiter"] = ";"

Given these parameters, the function call can be made to write the file in csv-format to the file system.

**Coding**
>
    fileAbsPath = para["Stem"] + para["Path"] + para["Basename"] + ".csv"
    df.to_csv(fileAbsPath, sep= para["Delimiter"], encoding="utf-8")

As a result, we find a new csv-file created on the file system.

{% include images/image.html imagePath = "../images/img_public/Accounts.png" imageCaption =  "Table saved as csv-file."%}

## Step 2: Read from a CSV-File









## Step 3: Save to an Excel

Specify the Sheet.

## Step 4: Read from an Excel


We want to create a table with accounts and months. All values shall be 0.
Let's put the months as columns and accounts as rows.

- At first, we create a list for the accounts.
- Second, a list for the months. 
- Third, we use the pandas command to create the dataframe using the accounts as index and the months as columns.
- Finally, we fill the values of the cells with zeros.




As intended, the output is a table.

**Output**
>
                January  February  March
    Account_A        0         0      0
    Account_B        0         0      0
    Account_D        0         0      0
    Account_X        0         0      0

---

This completes the first part.
In summary, we created a simple table realized as a Pandas dataframe.

## Step 2: Make the columns more dynamic
Previously, we created some tables. Now it is time to save them.
We only save to the file system. A database is not needed at this stage. Much further down the road there comes a point in time when adding functionality would become equal to rewriting a database. Then, it is worth considering to use an existing database.
Here we handle, for a table in dataframe format
    • Write to a csv-file
    • Read from a csv-file
    • Write as a Excel
    • Read from Excel

Step 1: Save to a CSV-File

Step 2: Read from a CSV-File

Step 3: Save to an Excel
Specify the Sheet.

Step 4: Read from an Excel
