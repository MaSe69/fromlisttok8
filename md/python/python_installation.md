---
layout: page_public
title: List to K8s
meta: Overview Meta
permalink: /python_installation/
---

# Installation

## Install Python

Here, only Python is used. 

If you want to use another programming language, you need to do the transfer work from Python to that other language, which should not be too difficult.

I do not describe Python installation here, because it is better explained and kept accurate by the respective experts. 
Bearing in mind to transfer that Python program to GCP later, the installation here is directed to this goal.

After installation of Python, check that you can get a "Hello World" on the terminal.

## Background on installation

It is very advisable to run a Python program in an environment. 
Recommendably, use pipenv 


### Install pip

<code>
sudo apt update
</code>


<code>
sudo apt install python3-pip
</code>

Check installation using

<code>
pip3 --version
</code>


### Install pipenv

<code>
sudo -H pip install -U pipenv
</code>


<code>
pipenv shell
</code>


## Python libraries

Libraries that are used in this context include
- matplotlib
- numpy

# References 

- [Python on Ubuntu](https://tecadmin.net/install-python-3-7-on-ubuntu-linuxmint/)
- [pip on Ubuntu](https://linuxize.com/post/how-to-install-pip-on-ubuntu-18.04/)

