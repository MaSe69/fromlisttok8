---
layout: page_public
title: List to K8s
meta: Overview Meta
permalink: /overview_20/
---

# Python

You need to decide to go for a
- Local program
- Web application

On your way to a public web application, you should not waste time on functionality that is going to be only available on some local machines.

However, there are very valid use cases for which data need to stay local. 
Sensitive data are a typically not propagaed to the web. 

Much functionality, in particular
- a user face for more convenient or consitent data maintenance
- graphical analysis
can be realized using Python libraries, usually much quicker than using a browser-based application. 

## Installations and Fundamentals

In any case, you need some fundamentals. 

What you need is Python:
- [Python - Installation](../python_installation)

Once Python is up and running, you need some data within Python data structures, and you need some functionality to process these data.

- [Python - Choose your types and structures](../python_data_structures)
- [Python - Upload your data](../python_upload_data)
- [Python - Process your data](../python_data_processing)


# Local program

Once you got some data, you might want to display them graphically.
Further, you might want to add some data, particularly without touching coding or creating files.

- [Python - Data Graphics](../python_graphics)
- [Python - Data Input UI](../python_input_ui)


## Web App Development - Local Deployment Only


- [Python - Flask](../python_flask)
