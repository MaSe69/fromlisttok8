---
layout: page_public
title: List to K8s
meta: Overview Meta
permalink: /list_operations/
---


# List 

## Definition


A "list" as defined here has as least two columns and several rows.
The upper row is the header that contains unique descriptions of the columns.
The left-most column contains unique text objects, the right-most column contains a numerical value.

Example:
Ingredient | Unit | Number
Eggs     | pieces | 6 
Butter | gramm | 250
Flour | gramm | 300

There are of course a lot of other types of lists. You might feel that confining the defintion as above is too much of a restriction, but it is most common in business application problems. Reduction is necessary here to advance at sufficent pace to the goal of global services.


## Limited List Size + Human Readability

Big Data is for good reason a buzz word since years. However, big data shall be out of scope here. 
The number of rows shall be 'manageable by humans' on a normal screen, i.e. at most a few hundred rows. However, typically more than 10 rows, because otherwise a list is often not worth the effort.

Similarly all entries shall be human readable. It is good business programming practice to use unique indentifies (UUIDs) in database tables. However, in most cases you are doing fine with entries that you can read, interprete and memorize easily.

As memory is cheap and of no limiting nature in this context, avoid abbreviations. The time you save writing is wasted many times later by trying to figure out what it meant at the time of writing. 
a.a. (avoid abbrevations)


# List - One to Many Relationships

In some lists, every entry is unique. 
Typically, however, some entries occur many times.

Example:
You want to weigh butter and flour together. First, you weigh the butter, then you add the flower. How many gramms does the gauge need to show? 


# One List

The most common questions to a list are
- How many rows?
- What is the sum?

In Excel, you find the row count, the sum and other standard aggregations in the status bar at the bottom.
Further, standard operations on a single list are
- Filter
- Sorting
They are pretty much self-explenatory.

## Checking for uniqueness

Uniquenss of fields are often very important.
The importance of checking for uniqueness is also generally under-estimated.

Example:
You job might be to collect money from people on a list. The list tells you the names and a flag for paid or not. You go down the list row by row and find that John Doe has not paid. You address John Doe on this topic and you get an angry reply that he already paid. Later, you find further down on the list another entry "John Doe" with a flag for payment done.

You can check for uniqueness in several ways. 
- Using the filter
- Using Pivot table
- Using Sort and Remove Duplicates.

My favorite is to copy the table, sort by the column that is to be checked for unique values. Then, you apply the function "Remove Duplicates". You get a info message telling you the result. You can also count the remaining number of rows. If it is lower than the original number of rows, the original table contained duplicates.


## Analysis + Pivot Tables

You can insert a graph. This functionality has such a good user interface that it is easier to use than to describe.

A very powerful and indispensible tool are the pivot table.
A Pivot table gives you the answer in the weighing example above: 550 gramms.


## Multiplications

You can multiply all values in the table with a value.

Example: 
The recipe was meant for 1 cake, but you need to bake 3 cakes. 
For making the shopping list, you multiply all value by 3.


# Splitting a list

Often, there is already a list.
Particularly a list with many columns.
Typically, only a few columns are needed.
Then, it is advisable, to create a new list from the old list.

A foreseeable problem can be that the reminder of the old list can change while you work on your part of the list. Hence, at a later point in time, it might be necessary to merge the lists again.
You therefore split a list using key fields. Key fields are a set of fields that make a row unique.

Example: 
You have a list with names. All names are unique. Then these names can be your key fields. Consider to check for uniquness.
If a uniqueness check reveals that there are two entries with John Doe, then you need an additional field. One John Doe might be from Dover and the other from Kent. Then, the name and the city can be key fields.


# Two Lists

Merging lists is the most important functionality. You might be rightfully reluctant on splitting lists when you are lacking experience on how to merge them again.

Lists that are sharing key fields can be merged automatically. 
Recommendably, you use the command vlookup for merging. 

Notes:
- The list need to be sorted.
- In Excel, this command has the default to return the nearest value, if the searched value is not found. Set this value to 'FALSE' if you really want to have NA returned when the value is not available in the other list.

