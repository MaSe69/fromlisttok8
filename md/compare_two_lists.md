---
layout: page_public
title: List to K8s
meta: Overview Meta
permalink: /compare_two_lists/
---

# Compare two lists

A common practical problem is two compare two lists on the same topic.
The two lists might contain the same data, particularly for the key field.

In the registration example, you might get another list of possible invitees.
The entries that occur more than once are so called 'duplicates'. 
In many cases, no harm is done by duplicates. Sending an email with the same recipient twice in the recipients list, still leads to only one email in his or her inbox.

In other cases, duplicates are annoying or even harmful. 
The simple task to report on the number of invitees gets more difficult, if the number of rows in the body of your list does not match that number.


## Removing duplicates 

Removing duplicates is one of the standard task of a list processing program, in particular of Excel.
The procedure of removing duplicates from excel has well been documented elsewhere. 
It comprises essentially two steps: 
- Sorting the data
- Apply the function 'remove duplicates'. 
-- You might get a choice on which columns to compare.

You get an information on how many rows were removed. 
If no duplicates were found, then your key fields have been unique already.


## Getting a list of unique fields from two lists

If you got two lists in which you know of, suspect or at least check for duplicates, you can proceed as follows:
- Combine the two lists such that the key field is in own column
- Sort that column
- Apply the function 'remove duplicates'. 














