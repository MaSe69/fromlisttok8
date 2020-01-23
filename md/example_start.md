---
layout: page_public
title: List to K8s
meta: Overview Meta
permalink: /example_start/
---

# Example

## The Story

You got the following task:

There is somebody or many, e.g. our boss, your team, your big family, who want to organize something. In business, he, she or they are called your stakeholders.
Your stakeholder wants to organize an event. Let's say an evening event. The invitees are known, e.g. members of the team, members of an organization, family members, customers. 
For cases when the invitees are not all known at the beginningm, see [Example for registrations](..//example_registrations).

However, it is not for free for the invitees. Invitees need to register by transferring a payment in advance. The payment turns an 'invitee' into a 'participant'.

Some time before the event, it needs to be decided, if the event should take place. The criterion is a minimum number of payments received. If there are sufficient participants, the participants shall get an invitation to the event.


## A straightforward, anonymous solution in practice

The problem above can be solved and was already solved in practice in the following way: 

- Somebody writes an email to 'all participants' including payment details until a deadline.
- An invitee does or does not transfer money until the deadline.
- After the deadline, somebody reports, if there are sufficient payments.
- The organization of the event is continued or discontinued.

In a basic scenario, it is sufficient to count the transfers on the receiving account on the deadline.
It is easier, if the scenario can remain 'anonymous', e.g. a second email after the deadline states:

"Dear invitees, the event will take place. If you have paid, you are welcome."


## Adding identities

The problem gets a bit tougher, when identities are required.
Your stakeholder suggests to 
- Remind invitees who did not pay some days before the deadline.
- Invite the participants.


## A list with identities

Typically, you would start with a list of invitees:

{% include images/image.html imagePath = "../images/img_public/fromlist2k8s_names.jpg" imageCaption =  "Typical list for invitees. Names were created by a random name generator for German names"%}

- Name of the invitee
- Paid or not paid











