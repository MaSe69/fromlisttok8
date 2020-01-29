---
layout: page_public
title: List to K8s
meta: Overview Meta
permalink: /python_data_structures/
---

# Python Data Structures for Lists

## Transfer of a first list to Python

Python has various data formats. 

You might be familiar to arrays. You can easily start with an array.

<code>
array = ["Marco Ehrlichmann"]
<br>
print(array[0])
</code>


Next, you could expand to nested arrays. 

However, in Python the "Dictionnary" structure is much more convenient and should be used. 

<code>
dict = {"Marco Ehrlichmann": 50, "Marina Schuster": 0} <br>
print(dict["Marco Ehrlichmann"])
</code>

You get the point how to expand the dictionnary to include all names and their payments. 
You would have to insert into the coding any change of payment. Obviously, this is more tedious and error-prone than maintaining the data in an Excel.

The benefit start with
on the input side
- automated data input
- data separation (master data, transactional data)
- more user friendly UIs
- data enhancements

and on the output side 
- data analysis
