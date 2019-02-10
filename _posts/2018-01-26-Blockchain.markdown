---
title: "Building a decentralized application" #TODO pictogram
layout: post
date: 2018-12-15 10:00
tag:
- Go
- Blockchain
- Decentralized systems
image: assets/images/blockchain.png # TODO picture
image-external: false
headerImage: true
projects: true
hidden: true # don't count this post in blog pagination
description: "Learning the basics of blockchain by building a decentralized application in Go."
category: project
#author: johndoe
externalLink: false
#TODO add github project
---

Learning the basics of blockchain by building a decentralized application in Go.
[Github Repository](https://github.com/MaxDimi/Peerster).

---

For the [Decentralized Systems Engineering](http://edu.epfl.ch/coursebook/en/decentralized-systems-engineering-CS-438) course at EPFL, I built a peer-to-peer application over UDP.
The main steps and functionalities were:
- **Gossiping protocol**: allow peers to communicate between each other and let them spread their messages through the network. They also need to keep track of the messages they already got, in order to ask for the ones they missed.
- **File sharing**: files can be uploaded and shared amongst peers.
- **File searching**: peers can search for files by using keywords, and download them when they are found.
- **Blockchain mining**: files are wrapped into blocks and then mined to ensure that no two different files share the same name. Consensus is reached through the Nakamoto protocol.

For the final step, we were free to extend the basic implementation with a functionality of our choice.
I added transfers with condition.
For this, I implemented a basic cryptomoney system, protected by public/private keys belonging to each peer.
Then, I created transfers and added them to the blockchain.
A block catch-up mechanism was also necessary to ensure that new peers that join the network later on can get the current history of transfers.
Finally, I allowed conditions to be set on transfers.
I picked time conditions, but other types could be easily added.
A peer can define either a deadline or a delay after which the transfer will be completed.

This project was very interesting and allowed me to learn a lot, both about Go (which I had never used before) and about decentralized applications.
It was a hands-on approach, which I really appreciated, and it sparked my interest for blockchain, smart contracts, and the multiple possibilities they offer.
