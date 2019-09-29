---
priority: 0.7
categories: works
options: [minihead]
layout: portfolio
title: Metropolis Lab
period: May 2017 to March 2019
location: Barcelona, Spain
icon: metropolis.png
---
#### Project

> “Bus-on-demand”: Similar to an e-hail application, but with a small bus and a flexible route, which introduces optimisation problems, as the system needs to ensure that the order of picking up and dropping passengers is (close to) the most optimal.

#### Role

I developed the back-end as a series of Kotlin services, all setup as listeners to events on a Firebase Realtime Database (part of Google Cloud Services), which acted as an event-bus. 

The route/scheduling optimisation module was initially written in R as a POC, and re-written by me in Kotlin. 

Routing information was provided by Google and by an instance of OSRM, running on a docker container on AWS. The kotlin services were deployed on Cloud Foundry.  A full simulation tool was also developed in kotlin to allow for testing and public demos. 



