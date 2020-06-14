---
layout: page_public
title: From Lists to K8s
meta: Overview Meta
permalink: /op_tables/
---

# Operations on Tables

In the previous sections, we saw how to

- create tables
- save tables to the file system - and read them again
- plot tables

In the following sections, we will see how to operate

- on tables
- on columns
- on rows
- on cells

As in all section, we follow the paradigm to operate on an 'original' table that we read from the file system before saving the modified table again to the file system.
The sequence is always:

- Read the table from file system. The 'Alpha'-Step.
- Modify the table by applying some operations to it.
- Write the modified table to the file system using another name or even into another folder. The 'Omega'-Step.

Just remember to start with Alpha and to end with Omega.


## Rename columns + Set index

The column names of our table saved on the file system originate from the automated creation of time periods.
Such names are unlikely to 'sound nice'. Let's make it a bit more comforable and give them shorter names that are easier to digest.

We define a list of the same length as the number of columns. Then, we set the columns of the dataframe to that list.

**Coding**
>
    myColumns = ['Account', 'Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun']
    df.columns = myColumns
    df = df.set_index("Account")

Finally, we set the index from the default created by Pandas to the dedicated column.


## Step 2: Local Copy

At first, we should make a local copy of the table that we read from the database. Be aware to make a real copy.

**Coding**
>
    df_New = df.copy()   # Create a copy 
>
    df_New = df          # Does not create a copy, just another name

A new window pops up that contains the plot.


## Step 3: Convert all numerical values

There is no need to convert entries like "123.45" on the csv-file into float.
Sometimes, another type, particularly integers are required.
It might be not enough to get rid of the decimals, which in the scenario here can represent cents, but also to round the integers to larger amounts.


**Coding**
>
    dfInt = dfInt.astype('int32').round(-1)


**Image**
{% include images/image.html imagePath = "../images/img_blog/opTables_Integers.png" imageCaption = "All values converted to integers and rounded to 10s."%}




## Step 4: Meta data about the dataframe

Often, we just need the number of columns or rows. Using 'shape' is one of several possibilities.

**Coding**
>
    print("Number of (rows, columns):", df.shape)
>
    dfMetaData = df.describe()
    dfMetaData = dfMetaData.astype('int32')

The command 'describe' returns meta data on the dataframe.

**Image**
{% include images/image.html imagePath = "../images/img_blog/Meta_data.png" imageCaption = "The mean values of the columns and much more statistics."%}


## Summary

The task was to explore a table in more detail.

Pandas enables to carry out meaningful operation on all cells - of a suitable type.
