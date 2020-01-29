---
layout: page_public
title: LIst to K8s
meta: Overview Meta
permalink: /overview_localprogram/
---

# Local program

## Motivation

Why would you convert an existing list into a local program?

Possible reasons:
- It is important
- It must be very accurate
- You want to double check your Excel result
- There is repetitive work that you want to automate in the future
- It is a step on your way to a public service


## Install Python

Here, only Python is used. If you want to use another programming language, you need to do the transfer work from Python to that other language, which should not be too difficult.

I do not describe Python installation here, because it is better explained and kept accurate by the respective experts. 
Bearing in mind to transfer that Python program to GCP later, the installation here is directed to this goal.

After installation of Python, you can get a "Hello World" on the terminal.

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

## Master data

Create a csv and upload it to your Python program.

## Transactional data

Use a random generator to simulate the usage of the program.

## Analyse the data

Loop over the final data to get results from which the original question can be answered.














