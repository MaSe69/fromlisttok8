---
layout: page_public
title: From Lists to K8s
meta: Overview Meta
permalink: /fromliststok8sservices/
---

# From Lists to K8s Services

Kubernetes is trendy. 
If you are a good programmer, you are expected to containerize your coding and to run it using Kubernetes.

However, Kubernetes comes with quite some overhead and it can be expensive when not applied correctly. Further, a considerable skill set is required and for the first projects additional time might be needed to figure out all necessary details.

This leads to the question, if containerization is really always necessary. If not, what would be appropriate steps leading to a containerized application.


# A Story and Examples

As the matter is complex, it is best to go on this journey with a story.
Taken from real life, I start with a simple example and evolve it slowly to complexity.
[Story and Examples](../example_start)


## Starting small - and sketching until it fits

A professional painter would never start with tiny details on a big painting.
First the overall contours must be established. Usually, assisting lines and structures are build which are erased during the process of completing the painting. 

Similarly, starting with details on containization or network optimizations seem the wrong end to start with, particularly when the overall application is far from being sure to be a business success. 

Lists in spreadshets like Excel or Libre Office are ideal for brain storming bigger applications.
Often, the lists prove to be sufficient to complete the job and no further development might be worth the effort. 

However, in some cases lists seems to develop a life on their own. They become ever more important,attracting interests of an increasing number of people, and finally tend to become overly complex.
In the end, people become annoyed with the lists and are asking for a "more advanced' way of completing the job.


## Producing code

Local development and testing is typically the starting point of producing code. 
At the same time, the goal of a containerized service should be kept in mind. This makes the succession from a local program to a globally available service much more efficient.

The step from a list to a first local program might be the most difficult one in the succession of steps suggested here. It already implies a lot of structure, particularly the separation in
- Database
- Application
- User interface

On the database layer, you might already want to distinguish between 
- master data
- transactional data

On the application layer, you might give it a though which are the core functionalities and how to keep them to a minimum such that extensions can be loosely added later. 

On the UI layer, you ideally implement a REST-like interface such that various UI technologies can interact with the data. 

## Going public, becoming expensive - and demanding revenue

Once you are leaving your own compute, you typically produce costs that either you or somebody else has to pay. Running a VM on a Cloud Provider is a typical example. 

On the other side, with a public service you substantially increase the service offering for others. Users might be willing to pay for using your service. 


## Adopting Cloud-Qualities

Based on an appropriate usage, you might want to increase your web application to be a true Cloud service. 
A Cloud service
- is nearly always there
- is innovative and constantly adopts to users' needs
- is interconnected with other valuable services in its context
- is as cheap as possible

The features above are technologically best realized by containerized software. Containers can be deployed to available hardware to make optimium use of that hardware. Hence, the overall costs for hardware usage gets minimized, and hence the costs for each serice can go down in principle. 
Together with a suitable architecture containers can make it easier for a larger application to continue to grow.
Kubernetes is the de facto standard to manage such containers. Kubernetes inherits from Google's Borg system. In general, many experts assess Google to be most advanced in this area. Hence, starting on GCP with containrization might be felt as a good and natural choice.







































