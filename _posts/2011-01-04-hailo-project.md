---
priority: 0.7
categories: works
options: [minihead]
layout: portfolio
title: Hailo
period: October 2010 to March 2017
location: London, UK
icon: hailo.png

---
#### Project

> “The evolution of hailing”: Hailo was one of the first e-hailing app. Before its merge with mytaxi, it had successfully delivered more than 20 million taxi journeys in thirteen cities in three continents. 

#### Role

I wrote all of the Java backend system, responsible for maintaining the network of drivers (location, status), finding the best drivers for a given customer, allocate jobs to drivers, and process driver payments.  A custom-built messaging system handle the communications between driver and customer app and the server. RabbitMQ was used to deliver messages and events, mySQL to store static data, and routino to provide routing information. The server were deployed on AWS instances throughout the world.

With time the system was completely transformed into a microservices platform written in Go, with hundreds of services. Despite already being CTO at the time, I wrote several Go services, such as: virtual meter (to be used in non taxi vehicles), fare calculator (to predict fare and compare with real ones).



