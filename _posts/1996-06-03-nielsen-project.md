---
priority: 0.7
title: Nielsen
categories: works
options: [minihead]
icon: nielsen.jpg
layout: portfolio
period: June 1996 to July 1999
location: Florida USA
---

#### Project

> AD*Views was a client-server application to allow access to Nielsen’s database of media audience. Product was licensed to TV stations and advertising agencies across the United States to track the performance of ads placed on different media. 

#### Role

I was hired as the sole C++ developer to maintain the tool. From day one the system presented problems, and after 6 months of intense fire-fighting, we decided that it was time to re-write it completely, observing more closely some fundamental principles of OO. 

The system was built as a free-form asynchronous reporting tool. Clients would request the data sliced in anyway they wanted, mixing years, media, and advertisers. The request was sent to the Database (acting as a message system at this point). The server periodically polled request from the database, and instantiate a reporting engine for each request. Once the query returned the data, it was assembled into a PowerBuilder object and sent back to the client (also via the db).

The effort involved a complete redesign and rewrite of more than 100K lines of C++ code, developing a system of parameterised queries that made the system faster, more reliable, and scalable, by applying OO design, and decoupling SQL from the C++ code. 


