---
title: system_design
date: 2020-11-29 15:31:10
tags:
---
1. What Are Design Fundamentals?
   relevant questions are vague, not objectively correct or incorrect, such as desigb uber by a 45-minute discsusion
   four categories:
   1. underlying or foundational knowledge(such as: how to kommunication between maschine, the protocol); 2. key characteristics of systems:avaliablility,wait and see, throughput, redundancy, consistency. 3. actual components of a system: load balancers, proxies, caches, rate limiting,leader election. 4. applying actual tech real exisiting products or services(Zookeeper, reddits, google cloud storage)


2. Client-Server Model
   how to kommunication between maschine?
   client: speak  to a server
   server: listens to a client and speak back to those clients
   Google brower make DNS query to find IP
   DNS(Domain Name System): specical requests, goes to a predetermined set of servers,  
   IP address: a unique identifiler for a maschine
   Ports: a maschine owns many ports, you must specify the concrete ones, when you want to communicate with that.
   HTML(Hypertext Markup Language): for documents designed to be displayed in a web browser
   e.g. when client communicate with Server via using the HTTP protocol. always port 80; HTTPS - port 443  local maschine's IP address

   Google brower sends an HTTP to Server to request this IP address
 
 3. Network Protocols 

    IP(Internet Protocol be made up of two parts:IP header and data((multiple)IP packets())) smallest units:bites; commen version: IPV(ersion)4,6
    TCP(Transmission Control Protocol,a more powewrful and more functional wrapper around IP;
    Function:ordering the packets of IP, virtually all web application) build on top of Internet Protocol.
    HTTP(HyperText Transfer Protocol): for request and response and visual

    TCP with the destin.maschine communication named as handshake(=specail TCP interaction)
    IP and TCP (at low level)for data transportation, while HTTP aims to add a lot of business logic

 4. Storage
    purpose:store od retrieve data
    gurantee: persistence of data
    Database: like as a server. Datebase writes data to disk(HDD or SSD), which cause to the persistence of data. 

 5. Latency and Throughput
    Latency: the times it takes for a certain operation to complete in a system.
             (RAM<SSD<Over Network< HDD< Round trip)
    Throughput:the number of operations that a system can handle properly per time unit

6. Availability
   
   Process: any process may get terminated at any time in a sufficliently large system
   a single maschine could act as a server for end users and as a client for a database
   Node/INstance/Host: a virtual or physical maschine on which the developer runs processes, like server
  
   Below are the downtimes expected per year depending on those 9s: 99.999%:5.2 minutes
   99% : 87.7 hours 

   Redundancy: the process of replicating parts of a system in an effort to make it more reliable

   SLA(service-level agreement) is made up of SLO(service-level objective) that is  a guarantee given to a customer by a service provider. SLOs typically make gurantees on a system's availability.

7. Caching

    Cache: a piece if hardware or software that stores data
    Cache hit: when requested data is found in a cache
    Cache Miss: used to refer to a negative consequence of a system failture or  if a poor design choice.

    Cache Eviction Policy: the policy by which values get evicted or removed from a cache, they include LRU(least-recently used),FIFO, LFU(least-frequently used).

    Content Delivery Network(CDN):  a third-party service that acts like a cache for your servers. often referred to as PoPs(points of Presence). A CDN has servers all around the world, meaning that the latency to a CDN's servers will almost always be far better than the latency to your servers. 
    popular CDN: Cloudflare and Google Cloud CDN