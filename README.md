# Blockchain IoT Academy Whitepaper

Visions for a futuristic learning experience

  * [Resources](#resources)
    + [Certification](#certification)
      - [Proof-of-Presence](#proof-of-presence)
      - [Proof-of-Development](#proof-of-development)
      - [Proof-of-Initiative](#proof-of-initiative)
- [Technology](#technology)
  * [DApplication](#dapplication)
    + [User Interface](#user-interface)
      - [Requirements](#requirements)
    + [API Specification](#api-specification)
      - [Requirements](#requirements-1)
      - [Endpoints](#endpoints)
        * [Account](#account)
        * [Project](#project)
        * [Certificates](#certificates)
        * [Interactions](#interactions)
    + [Nodes](#nodes)
      - [Requirements](#requirements-2)
      - [Dependencies](#dependencies)
    + [Database and Storage](#database-and-storage)
      - [Requirements](#requirements-3)
  * [Distributed Ledger](#distributed-ledger)
    + [Introduction](#introduction)
    + [Consensus](#consensus)
      - [1. Proof of Work](#1-proof-of-work)
      - [2. Leader-based systems](#2-leader-based-systems)
      - [3. Proof-of-Stake](#3-proof-of-stake)
    + [Protocol](#protocol)
      - [Introduction](#introduction-1)
      - [Directed Acyclic Graph](#directed-acyclic-graph)
      - [Whisper Protocol](#whisper-protocol)
      - [Hashgraph Consensus](#hashgraph-consensus)
  * [Internet of Things](#internet-of-things)
    + [Introduction](#introduction-2)
    + [Requirements](#requirements-4)
      - [Arduino](#arduino)
      - [Amazon FreeRTOS](#amazon-freertos)
    + [Things](#things)
      - [Sensors](#sensors)
        * [RFID](#rfid)
        * [Fingerprint](#fingerprint)
        * [iBeacons locations](#ibeacons-locations)
      - [Security](#security)
        * [Certificates](#certificates-1)
    + [Security](#security-1)
    + [Modules](#modules)
    + [Viable solutions:](#viable-solutions)
  * [References](#references)

<!-- tocstop -->

## Resources

- Cohorts
- Locations
- Programs
- Streams
- Participants
- Projects
- Certificates

### Certification

1. Proof-of-Presence
2. Proof-of-Development
3. Proof-of-Initiative

#### Proof-of-Presence
- Number of IoT interactions

#### Proof-of-Development

Automatic certificate verification based on the actual state of all transactions

Verification process
- Project submitted to the ledger
- Score > 70% of total final votes
- IoT devices interactions
- Hours committed
- Github repository with more than X commits

#### Proof-of-Initiative

- Number of specific interactions in the blockchain


# Technology

Components

1. Mobile Application
2. Distributed ledger
3. Internet of Things
4. RFID/Fingerprint

## DApplication

1. User Interface
2. API Specification
3. Nodes
4. Database and Storage

### User Interface

To be designed

#### Requirements

- Mobile Hybrid App for iOS/Android
- Javascript/HTML5/CSS
- Hybrid Application
- AngularJS
- Realtime sockets
- Objective-C
- iBeacon Library
- Push Notifications
- Local Storage

### API Specification

#### Requirements 
1. RESTFul An architectural style called REST (Representational State Transfer) advocates that web applications should use HTTP as it was originally envisioned. Lookups should use GET requests. PUT, POST, and DELETE requests should be used for mutation, creation, and deletion respectively.

- JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is easy for humans to read and write. It is easy for machines to parse and generate. It is based on a subset of the JavaScript Programming Language, Standard ECMA-262 3rd Edition - December 1999.

- Hypertext Transfer Protocol (HTTP) Status Code Registry

    - 1xx: Informational - Request received, continuing process
    - 2xx: Success - The action was successfully received, understood, and accepted
    - 3xx: Redirection - Further action must be taken in order to complete the request
    - 4xx: Client Error - The request contains bad syntax or cannot be fulfilled
    - 5xx: Server Error - The server failed to fulfill an apparently valid request


#### Endpoints

##### Account
    POST /account/create
    POST /account/identify/{publickey}
    PUT  /account/update
    GET  /account/me

##### Project
    POST /project/create
    PUT  /project/update
    POST /project/submit
    POST /project/{hash}/vote/{score}
    GET  /project/{hash}
    GET  /project/{hash}/votes

##### Certificates
    POST /certs/create
    POST /certs/issue

##### Interactions    
    POST /position/create
    POST /position/location/proximity

### Nodes

#### Requirements

1. Node.js
2. Express
3. Docker
4. Vagrant
4. NTP

Description

- Node.js is an open-source, cross-platform JavaScript run-time environment for executing JavaScript code server-side. 

- Docker is a software technology providing operating-system-level virtualization also known as containers, promoted by the company Docker, Inc.

- Vagrant is an open-source software product for building and maintaining portable virtual software development environments, e.g. for VirtualBox, Hyper-V, Docker, VMware, and AWS.

- Network Time Protocol (NTP) is a networking protocol for clock synchronization between computer systems over packet-switched, variable-latency data networks. In operation since before 1985, NTP is one of the oldest Internet protocols in current use. 

- NGINX is a web server which can also be used as a reverse proxy, load balancer and HTTP cache.

#### Dependencies

- Express is a minimal and flexible Node.js web application framework that provides a robust set of features for web and mobile applications.

- Sockets - Read and write

- AWS IoT 


### Database and Storage

- BigChainDB allows developers and enterprise to deploy blockchain proof-of-concepts, platforms and applications with a scalable blockchain database, supporting a wide range of industries and use cases.

- IPFS: A peer-to-peer hypermedia protocol
to make the web faster, safer, and more open.



#### Requirements

- MongoDB is a free and open-source cross-platform document-oriented database program. Classified as a NoSQL database program, MongoDB uses JSON-like documents with schemas.

- Python 3.5+

- Ubuntu Server 16.04 LTS

-- 

## Distributed Ledger

1. Introduction
2. Consensus
3. Protocol


### Introduction

Blockchains are inherently decentralized systems which consist of different actors who act depending on their incentives and on the information that is available to them.

Whenever a new transaction gets broadcasted to the network, nodes have the option to include that transaction to their copy of their ledger or to ignore it. When the majority of the actors which comprise the network decide on a single state, consensus is achieved.

### Consensus

1. Proof of Work
2. Leader-based system
3. Proof of Stake

#### 1. Proof of Work
If you have Proof-of-Work, then you’re going to need to use a lot of electricity. All of the miners will eventually migrate to where electricity is cheap, and then that government has the ability to destroy you. It’s just inevitable. This is why everyone is so desperate to move away from Proof-of-Work.


#### 2. Leader-based systems
Many permissioned (non-public) networks out there right now are built on these Leader-Based systems. In a Leader-based system, everybody in the network sends their transactions to a designated leader, and then that leader just picks an order [of transactions] to then send back out to the network. 

There are, however, several problems with this. If you have a distributed denial of service (DDoS) attack on the leader, the whole network collapses just by shutting down one computer. 

In some cases, there could be protection mechanisms in place to keep the network running with a leader shut down, however, other problems could arise if a virus in the system knows who the next leader is and can direct the botnet to attack this new leader – essentially, the botnet ends up playing “follow the leader”. 

So, with Leader-based systems, you can shut down the whole network by shutting down one computer at a time.

#### 3. Proof-of-Stake
Other consensus-forming systems have Proof-of-Stake in the name, but these are what people are usually referring to as these new economy-based systems. Proof-of-Stake is just anything that involves weighting by cryptocurrency. 

Everyone in the community actually gambles real money – real cryptocurrency – on what they think the consensus should be. 

In theory, anyone who votes with the majority gets more money, and anyone who votes with the minority loses some money. The idea is “we’re all motivated to vote with the majority – we’ll all be listening carefully to everyone else and trying to vote with the majority – then, Adam Smith’s invisible hand does its work, and we all reach consensus”.

With these Proof-of-Stake systems, though, you don’t even have as much of a math proof of security as you do for the Leader-Based systems. You could have instabilities – we don’t have any math proofs for how it can survive certain attacks. For this kind of Proof-of-Stake, we currently have all sorts of questions about how secure it is.

To advance and move away from Proof-of-Work, the blockchain community is proposing lots of variants of Proof-of-Stake, and typically what you find is a combination under the hood of something that’s partially Leader-Based also.

### Protocol

#### Introduction

1. Directed Acyclic Graph
2. Whisper Protocol
2. Hashgraph

#### Directed Acyclic Graph

With the Directed Acyclic Graph (DAG), each transaction forms a new block and it is verified by itself. To be able proceed this verification it has to first verify two randomly chosen transactions in the network.

This model has one more benefit. There is no limit for scaling. The problem that we face right now with cryptocurrencies (based on blockchain) is scalability. 

The DAG network could become indefinitely scalable with zero cost because every new transaction verifies two new transactions in the network. One more and more people join and send transaction, the network will grow and scale smoothly. A DAG brings solution for scalability with zero cost, that is revolutionary!

Why is DAG better than blockchain? Because DAG technology enables various features like zero-cost transactions, infinite scalability or offline transactions that blockchain simply cannot do and will neither probably be developed to do.

- No mining
- No blocks
- No difficulty
- No transaction fees
- Zero transaction costs
- Scales almost infinitely
- Machine efficiency
- Low-cost
- Potential for indefinite scalability
- Offline transactions

#### Whisper Protocol

In a nutshell whisper is a communication protocol for DApps to communicate with each other.

**Use cases**

- DApps that need to signal to each other in order to ultimately collaborate on a transaction. For example, a currency exchange DApp may use it to coordinate an offer prior to creating one (or two, depending on how the exchange is structured) transactions on the exchange.
- DApps that need to provide non-real-time hinting or general communications between each other. E.g. a small chat-room app.

**Specifications**

- Low-level API only exposed to DApps, never to users.
- Low-bandwidth not designed for large data transfers.
- Uncertain-latency not designed for RTC.
- Low-latency, 1-1 or 1-N signalling messages.
- High latency, high TTL 1-* publication messages.
- Messages less than 64K bytes, typically around 256 bytes.


#### Hashgraph Consensus
Directed Acyclic Graph Hashed + Whisper Protocol

Hashgraph is a new consensus alternative to the blockchain. It uses a gossip protocol that works in the following manner: 

Every node in Hashgraph can spread signed information (called events) on newly-created transactions and transactions received from others, to its randomly chosen neighbours.

These neighbours will aggregate received events with information received from other nodes into a new event, and then send it on to other randomly chosen neighbours. 

This process continues until all the nodes are aware of the information created or received at the beginning. Due to the rapid convergence property of the gossip protocol, every piece of new information can reach each node in the network in a fast manner.



## Internet of Things

1. Introduction
2. Requirements
3. Things

### Introduction

The Internet of Things (IoT) is a term coined by Kevin Ashton, a British technology pioneer working on radio-frequency identification (RFID) who conceived a system of ubiquitous sensors connecting the physical world to the Internet. 

Although things, internet, and connectivity are the three core components of IoT, the value is in closing the gap between the physical and digital world in self-reinforcing and self-improving systems.

### Requirements

#### Arduino

Open-source electronic prototyping platform enabling users to create interactive electronic objects.

#### Amazon FreeRTOS 
FreeRTOS is an operating system for microcontrollers that makes small, low-power edge devices easy to program, deploy, secure, connect, and manage. 

Amazon FreeRTOS is based on the FreeRTOS kernel, a popular open source operating system for microcontrollers, and extends it with software libraries that make it easy to securely connect your small, low-power devices to AWS cloud services like AWS IoT Core or to more powerful edge devices running AWS Greengrass.


### Things

#### Sensors

##### RFID

##### Fingerprint

##### iBeacons locations

- Labs
- Entrance
- Coffee machine
- Restaurant

#### Security

To make IoT ecosystem secure, we need to think about machines and devices differently, not just as a metal things without life. We need to consider each device as its own identity.

Why? Because the identity carries some attributes and we cannot securely and efficiently work with IoT without knowing more.

One of the biggest challenge for IoT will be the maintenance. Creation is hard process, but to maintain IoT (means also keep them resilient) is a long-term task, that cannot be undervalued. Look at any software and application that you use on PC or smartphone. How many times did you update it? Maintenance is a new angle of re-creation process.

Identity of Things will become a new standard. The question is when it will happen. To give you an idea, we need to create IoT with some specific attributes, such as:

- who manufactured it
- when it was deployed
- what is the expected life time cycle
- who owns it
- what data is it gathering

##### Certificates

AWS IoT authenticates certificates using the TLS protocol’s client authentication mode. TLS is available in many programming languages and operating systems and is commonly used for encrypting data. 

In TLS client authentication, AWS IoT requests a client X.509 certificate and validates the certificate’s status and AWS account against a registry of certificates. It then challenges the client for proof of ownership of the private key that corresponds to the public key contained in the certificate.


X.509 certificates are digital certificates that use the X.509 public key infrastructure standard to associate a public key with an identity contained in a certificate. X.509 certificates are issued by a trusted entity called a certification authority (CA). The CA maintains one or more special certificates called CA certificates that it uses to issue X.509 certificates. Only the certification authority has access to CA certificates.




### Security

Far by most important is security. As our society technologically grow, we became dependant on software and hardware. We become more vulnerable to software or hardware malfunction or hacker's attacks. The future will take place even more in cyberspace, so security should be our first priority when we aiming for a tech change.

Quantum computation and mechanics cause headaches to security engineers, because in the coming decades we can see very real possibility of scalable quantum computers. This will disrupt most of cryptographic protocols used today. So in another words, our world can become insecure with quantum computers. 

### Modules
1. Community
Resume of last activities in the blockchain

2. My account
Import/export keys

3. Projects
List and voting

4. Analytics
Useful reports


### Viable solutions:

1. RFID Card Scanner
2. Fingerprint


## References
IOTA
https://medium.com/@MartinRosulek/how-iota-makes-future-for-internet-of-things-af14fd77d2a3

Whisper
https://github.com/ethereum/wiki/wiki/Whisper

Hashgraph
https://www.hiddenforcespod.com/leemon-baird-hashgraph-distributed-ledger-technology-blockchain/

Byzantine
https://medium.com/loom-network/understanding-blockchain-fundamentals-part-1-byzantine-fault-tolerance-245f46fe8419

AWS IoT
https://aws.amazon.com/iot/


