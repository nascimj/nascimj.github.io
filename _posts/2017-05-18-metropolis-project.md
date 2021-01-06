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

Firebase is extremely simple to setup, and has great support for services to act as listeners. In Kotlin (or Java) you simply inherit from a class like 
```kotlin
com.google.firebase.database.ChildEventListener
``` 
and define your methods to respond to, such as:
```kotlin
    onChildMoved
    onChildRemoved
    onChildChanged
```

>I think the really cool thing about Firebase is that it is equally easy to setup an App as a listener (on both IoS and Android). That allows the apps to be active participants in the event flow.


The route/scheduling optimisation module was initially written in R as a POC, and re-written by me in Kotlin. 

Routing information was provided by Google (via their regular API) 

> Google's routing api is great, but it is becoming increasingly costly to use. In our case we did not expect a high usage, but to be safe (and to learn a bit) I built and deployed an instance of [OSRM](http://project-osrm.org/) with a map of Germany to AWS on a docker container. The results were good enough. The main problem with using OSRM is the need to build an update routine (to get new maps), and the fact that it takes a lot of resources. A country as large as Germany was enough to keep our AWS instance very busy.


The kotlin services were deployed on Cloud Foundry.  A full simulation tool was also developed in kotlin to allow for testing and public demos. 

> I love building simulations, and they are great for demos in conferences, or big presentations to the board. This one would allow us to create buses around the city, and set them in movement. From that point on, the apps could interact with the simmulation as if it was a real bus, as it would respond to booking requests, re-route, etc.



