---
layout: post
title:  "Understanding RPL"
date:   2020-08-30 17:19:03 +1000
categories: learning cs
---

For an upcoming potential job it was suggested that I do some reading on RPL (Routing Protocol for Low-Power and Lossy Networks). Half an hour of reading later, I was still thoroughly perplexed on what all the terms or concepts even meant! Clearly it was time to do my very first networking course. 

The OSSU curriculum includes an [Introduction to Computer Networking](https://www.youtube.com/playlist?list=PLEAYkSg4uSQ2dr0XO_Nwa5OcdEcaaELSG) course, which strangely links to a YouTube playlist of two guys sitting on a couch. From what I can gather the videos are from a Stanford course that was originally available but the Lagunita online learning platform was retired earlier this year. The two alternatives I saw recommended were a [Georgia Tech Udacity course](https://www.udacity.com/course/computer-networking--ud436) and a [Google Coursera course](https://www.coursera.org/learn/computer-networking), more advanced and less advanced than the Stanford course respectively. 

I followed both the Stanford and Coursera at first, but I found that the Coursera course had a smoother difficulty curve with more production value as well, and ultimately stayed with that one. As I had limited time, I focused on the basic topics such as the internet layer model, TCP, packet switching, encapsulation and error detection, before skipping ahead to learning about ethernet and wireless networking.

Equipped with my new knowledge, I returned for a second attempt at understanding RPL, which I actually found much easier this time around. Here's my attempt at simplifying the information as much as possible: 

## Acronyms
- DODAG - Destination Oriented Directed Acyclic Graph (has a root and no cycles)
- DIS - DODAG Information Solicitation (solicits information from other nodes)
- DIO - DODAG Information Object (information sent downstream to other nodes)
- DAO - Destination Advertistment Object (provides destination information upwards)

## Trickle timer
- When a node's data does not agree with its neighbours it communicates quickly to resolve the inconsistency. When they agree, they slow communication exponentially.

## Joining
1. A node that wants to join a network will transmit periodic DISs
2. Neighbouring nodes reset their trickle timer in response and send out DIOs more often
4. Joining node receives DIOs and probes links with neighbours to select preferred parent with shortest link to the root
5. Node registers itself via a DAO that is sent to the parent and forwarded until it reaches the root
6. Node receives a DAO-ACK, is not part of the network and starts advertising DIOs in turn on a trickle timer

## DAG Maintenance
- Nodes constantly probe neighbours to maintain updated link estimates
- Keeps preferred parent up to date e.g. if the link between a node and its parent becomes bad, the node may switch parents
- When a node finds no more suitable parents it will let its children know it's no longer a valid parent and then leave the network after a delay
- Meanwhile it starts sending perioding DIS again hoping to discover a new usable parent

Next step: try and explain to concepts above to someone!