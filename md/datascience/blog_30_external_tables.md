---
layout: page_public
title: From Lists to K8s
meta: Overview Meta
permalink: /external_tables/
---

# Blog 1: Create Tables

Previously, we created some tables. Now it is time to save them.

We only save to the file system. A database is not needed at this stage. Much further down the road there comes a point in time when adding functionality would become equal to rewriting a database. Then, it is worth considering to use an existing database.

Here we handle, for a table in dataframe format

- Write to a csv-file
- Read from a csv-file
- Write as a Excel
- Read from Excel

## Step 1: Save to a CSV-File

**Coding**
>
    accounts = ["Account_A", "Account_B", "Account_D", "Account_X"]
    months = ["January", "February", "March"]
    df = pd.DataFrame(index=accounts, columns=months)
    df = df.fillna(0)

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
