---
layout: page_public
title: From Lists to K8s
meta: Overview Meta
permalink: /ds_overview/
---

# Overview

In a series of blog, I want to compare Python Pandas to Microsoft Excel.

Why would you learn and upskill to Python Pandas, if you got Excel? You might rightfully ask.

In this first part, let me try to give an answer to this question. 

In the following parts, I will detail out those parts of Python Pandas that I used to make the move from Excel. At the end of each part, there will be a listing of the program output. Hence, by browsing through these results you can make your own assessments.
“Most companies are run using Excel”, I was once told. My 20+ years’ experience confirm this. Excel is a most powerful tool. It is hard to find a use case that you cannot cover using Excel. You have no set-up time, get quickly to the first successes and you can expand your skills when needed. I saw and worked with elaborate and powerful Excel sheets, which took rather months than weeks to create.

However, there are also quite some downsides. For larger tasks, questions usually comes up like

- Shouldn’t we move to an existing software solution for this particular problem?
- Shouldn’t we use a database?

Apparently, for any problem you encounter in business life, there is a software solution around, usually plenty of them. However, moving to any of these solution is always quite some investment. It takes time to have an equivalent functionality in the new software, then this solution should be used for a reasonable amount of time. Crucially, moving to a specific software feels like losing flexibility. Typically, for many tasks, this move is not done and everybody muddles on in Excel. 
What might be needed is a solution in this niche, providing

- Keeping the flexibility of a spread sheet 
- Providing the optimization potential of a program.

## Python

The programming language Python in combination with its add-ons, particularly Pandas fills this niche. It is certainly not the only player in this niche. As the favored combination in data science, Python and Pandas is a combination you should be aware of when you want to move in this direction.
The programming language Python has been around for many years. Details can be easily found. An important point might be the revival Python experienced possibly in the context of Big Data and Artificial Intelligence. Python had got an image as a rather inferior language, confined to an entry level – not the right tool for a serious, professional developer. In recent years, massive investments in Python took place, Python applications increased in values and the salaries for Python developer also increased considerably.
On top of Python, an abundance of library have been provided. Many libraries are dedicated to operations on data. These libraries turn Python into a surprisingly powerful tool. 

## Pandas

The library in the focus here is Pandas, see for the [Pandas](https://pandas.pydata.org/) .
According to its mission: “[...] Pandas aims to be the fundamental high-level building block for doing practical, real world data analysis.”
 “Pandas is a software library written for the Python programming language for data manipulation and analysis. In particular, it offers data structures and operations for manipulating numerical tables.”
The pandas documentation is not repeated here. Here, it is about using Pandas for data science.

At the heart of Pandas is an object called “data frame”, which is in this context here essentially a table. Two-dimensional DataFrame can be made to have unique keys in the rows and named headers. 
Pandas is often used within a Jupyter notebook. Commands are entered one by one and immediately a result is returned. This combination is a valid use case particularly for a quick data validation. For a long-term optimization, embedding Pandas in Python scripts appears to be the more adequate tool.

## A reminiscense to ABAP

‘Pandas table’ can have some similarities with “internal tables” known from SAP’s programming language ABAP. In this sense, programming in Python can become quite similar to development ABAP. Many ABAP developer value highly the efficiency of those internal tables. With Pandas, it is possible to become similarly efficient.
For the demonstration, I chose two scenarios:

- A more business-like scenario on accounting
- A more recreational scenario on ratings

The accounting scenario shall have accounts and months. Sums shall be computed for accounts and months.
The rating scenario shall have ratings and users. The ranking of the objects, e.g. movies, shall be determined.