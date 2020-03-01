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
- select a zone 
- select the operating system
- select a machine type 
- accept HTTP and HTTPS requests

After the VM is available
- SSH into your VM


## Installations on the VM

Python is already installed.

- Install pip
- Install Flask

Optional:
- Install an editor, e.g. PyCharm
- Configure link to GitHub.com


## Flask

- Copy+Paste an existing Flask application to the editor running on the VM
- Run the Flask application
- Test the Flask app with the external IP.

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

GitHub:
For private repositories, you need to take care of SSH keys.

<code>
git pull repo
</code>
