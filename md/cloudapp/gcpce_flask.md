---
layout: page_public
title: List to K8s
meta: Overview Meta
permalink: /gcpce_flask/
---

# Simple Flask App on GCP Compute Engine


## Create a VM on Compute Engine

In Compute Engine, choose VM instances.

On the tab "Create an instance", 
- type a name for your VM
- select a zone (nearest to you or cheapest)
- select a machine type (for development, the cheapest one will do)
    - micro, f1
- on firewall, tick at least HTTP, or also HTTPS

Push button 'Create'. 
Wait, until the VM is created.


## Create the flask flile

SSH into your VM

<code>
vim server.py
</code>



Install pip

<code>
sudo easy-install pip
</code>

Install Flask

<code>
sudo pip install flask
pip3 install flask
</code>

Run the Flask application

<code>
sudo python server.py
</code>


## References

- [GCP Cloud Engine Documentation](https://cloud.google.com/python/tutorials/getting-started-on-compute-engine)


- Use ssh to install software on your VM.
- Connect to your Github repository
- Run your app

[YouTube - Running Flasks aps on Google Cloud Engine](https://www.youtube.com/watch?v=4YAiPgJPC0A)

- Create a project
- Create an instance of a VM (Use Compute Engine Quickstart)
-- Choose an operating system (OS)
-- Firewall: Allow HTTP(S) traffic
-- SSH: Open in browser window

Commands
sudo apt-get install python-setuptools
sudo easy_install flask markdown

GitHub:
For private repos, you need to take care of SSH keys.

<code>
git pull repo
</code>
