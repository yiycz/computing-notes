# Short Summary of Computing Syllabus

## 1. Algorithm, Pesudocode, Flowchart and Decision Table

### Definitions

**Algorithm**

An algorithm is a step-by-step procedure (well-defined instructions) to solve a given problem.

**Pesudocode**

Pseudo code is a description of the steps in an algorithm using natural language (such as English) mixed with sequence, selection and iteration constructs.

### Applications

* Data types
* Declaring a variable
* Reading input
* Outputting
* Assignment
* If statement
* While loop
* For loop
* Case statement
* Arrays
* File Handling
* Modules/Subroutines
* Declaring Global variables
* Classes
* Bubble Sort as an example

---

## 2. Computer Network

### Definitions

**Computer Network**

A computer network is a system of two or more computers that are connected together by a transmission medium for the exchange of data.

**LAN (Local Area Network)**

A Local Area Network (LAN) is a network that connects computers and other devices within a limited geographical area, such as a home, office, or school. This allows devices to communicate and share resources at high speeds.

**WAN (Wide Area Network)**

A Wide Area Network (WAN) is a network that connects multiple LANs over large geographical areas, such as cities, countries, or continents, using communication links provided by telecommunications companies or Internet Service Providers (ISPs).

**Metropolitan Area Network (MAN)**

A metropolitan area network (MAN) is a network of computing devices covering a larger geographical area (two or more buildings within the same town or city) than a LAN. A MAN is typically owned and operated by a large organisation such as a cities, business or government body.

**Intranet**

An intranet is a private network built within an organisation, like a company, school, or government agency.

**Internet**

The internet is a global, public network accessible to anyone with an internet connection. It is a network of networks linked by a broad array of electronic, wireless, and optical networking technologies. It is essentially an infrastructure that provides services to applications.

**Nodes**

Any device or computer that can connect to a network and generate, process, or transfer data.

**Network topologies**

the physical or logical arrangement of devices (nodes) and connections (links) in a computer network that dictates how data flows

**Wi-Fi**

Wi-Fi is a wireless networking technology based on the IEEE 802.11 family of standards that allows devices to connect to a Local Area Network (LAN) using radio waves instead of physical cables.

**WLAN (Wireless Local Area Network)**

A Wireless Local Area Network (WLAN) is a Local Area Network (LAN) in which devices communicate wirelessly using Wi-Fi (IEEE 802.11) instead of Ethernet cables.

**Network Interface Card (NIC)**

A Network Interface Card (NIC) is a hardware component that enables a device to connect to a network by transmitting and receiving data. It provides the physical or wireless interface between the device and the network and is assigned a unique MAC (Media Access Control) address.

**Hub**

A device that connects multiple devices in a local network and blindly broadcasts data to all devices in the network.

**Switch**

A switch is a networking device that connects multiple devices (e.g. computers, printers, servers, access points, etc.) in a LAN (Local Area Network). Its purpose is to receive data from one device and send it to the intended destination.

**Router**

A router is a networking device that routes data packets between computer networks. It also directs traffic, choosing the best route for information to travel across the network so that it’s transmitted as efficiently as possible.

**Modem**

A modem is a network device that demodulates signals on the WAN side into digital data for the local network and modulates digital signals from the LAN to signals to be transmitted to the WAN.

**Wireless Access Point (WAP)**

A Wireless Access Point (WAP) is a networking device that allows wireless devices to connect to a wired LAN using Wi-Fi.

**IP Address**

An IP (Internet Protocol) address is a logical numerical address assigned to a device on a network, used to identify the device and enable data to be routed between different networks.

**Subnet Mask**

A subnet mask is a $32$ bit number used in IPv4 networking that helps divide an IP address into two components: the network portion (netID) and the host portion (hostID).

**CIDR Notation**

The Classless Inter-Domain Routing (CIDR) notation is a compact method of writing an IP address and its associated subnet mask.

**DHCP (Dynamic Host Configuration Protocol)**

The DHCP (Dynamic Host Configuration Protocol) is the protocol that automatically assigns IP addresses and other network settings to devices when they join a network.

**MAC Address**

A MAC (Media Access Control) address is a unique $48$-bit hexadecimal identifier assigned to a Network Interface Card (NIC), allowing devices to be identified and communicate on a Local Area Network (LAN).

**Packet**

A packet is a unit of data at the Network Layer (`Layer 3`) of the OSI Model that contains a payload and logical addressing information (Source and Destination IP addresses), allowing data to be routed between different networks.

**Packet Switching**

Packet Switching **is a method of sending data across a digital network by breaking files into small blocks called packets, which travel independently and share network resources dynamically.**

**Circuit Switching**

Circuit Switching is **a method of communication that sets up a dedicated communication path (or circuit) between the sender and receiver before any data moves. The path remains reserved for the entire communication session.**

**DNS (Domain Name System)**

It translates human-readable website names (like google.com) into machine-friendly IP addresses (like 192.168.1.1) so browsers can load internet resources. DNS uses port 53.

**DNS Server**

A DNS server maintains databases containing IP addresses and their corresponding domain names.

**HTTP**

HTTP (HyperText Transfer Protocol) is **an application-layer protocol used for communication between a client (such as a web browser) and a web server**.

**FTP**

FTP (File Transfer Protocol) is an **application-layer protocol specifically designed for transferring files between a client and a server over a network.**

**TCP/IP Model**

The Transmission Control Protocol/Internet Protocol (TCP/IP) model **is the fundamental framework for communication across the internet.** It defines how data is broken down, addressed, routed, and delivered between devices.

**OSI Model**

The OSI (Open Systems Interconnection) model is a 7-layer conceptual framework that standardises how data is transmitted between devices over a network by dividing network communication into separate layers, where each layer performs specific functions and provides services to the layer above it.

### Advantages

**LAN**

* High Speeds
* Low Latency
* Easy resource sharing
* More secure since its privately managed
* Relatively inexpensive

**WAN**

* Connects distant locations
* Enables global communication
* Support remote work
* Centralised data management

**Wired NIC**

* Faster and more stable
* Lower latency
* Less susceptible to interference

**Wireless NIC**

* No cables needed
* Mobile
* Easy to install

### Limitations

**LAN**

* Limited coverage
* Requires network equipment (switches, cables, routers, etc.)
* Network failure can affect many users

**WAN**

* Higher cost
* Higher latency
* More complex to manage
* More security risks because data often travels over public infrastructure

**UDP**

* Connectionless, efficient but unreliable transmission of packets
* If any packets are lost, they are lost forever

**Packet loss**

* At times, some routers may receive packets faster than they are able to route them on.
* These packets are buffered in memory and this introduces delays (referred to as a 'high latency').
* If the buffering is severe, the router may run out of memory and packets are simply discarded.

### Differences

#### Intranet vs Internet

| Feature        | Intranet                                                                    | Internet                                                                 |
| -------------- | --------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| **Scope**      | Private network within an organization                                      | Public network accessible globally                                       |
| **Access**     | Restricted to authorized users within the organization                      | Open to anyone with an internet connection                               |
| **Content**    | Internal resources relevant to the organization (documents, portals, tools) | Diverse content from various sources (news, social media, entertainment) |
| **Security**   | More secure due to restricted access                                        | Less secure due to open nature                                           |
| **Connection** | Can be isolated from the internet or connected with security measures       | Connects devices across the globe                                        |
| **Purpose**    | Internal communication, collaboration, secure resource sharing              | Global communication, information sharing, access to online services     |

#### Hub vs Switch vs Router

| Network Device | OSI Layer           | Uses               | Forwards                               |
| -------------- | ------------------- | ------------------ | -------------------------------------- |
| Hub            | Layer 1 (Physical)  | Electrical Signals | Bits                                   |
| Switch         | Layer 2 (Data Link) | MAC Addresses      | Unchanged Ethernet Frames              |
| Router         | Layer 3 (Network)   | IP Addresses       | Ethernet Frames with new MAC Addresses |

#### IP Address vs MAC Address

| IP Address                        | MAC Address                    |
| --------------------------------- | ------------------------------ |
| Logical address                   | Physical/Hardware address      |
| Network Layer `(Layer 3)`         | Data Link Layer `(Layer 2)`    |
| Used for routing between networks | Used for delivery within a LAN |
| Can change                        | Usually fixed                  |
| Assigned by DHCP/admin            | Assigned by manufacturer       |
| Used by routers                   | Used by switches               |

#### Packet Switching vs Circuit Switching

| Feature           | Packet Switching                                   | Circuit Switching                                      |
| ----------------- | -------------------------------------------------- | ------------------------------------------------------ |
| **Data Transfer** | Breaks data into packets, sent independently       | Dedicated path established between sender & receiver   |
| **Routing**       | Packets can take different routes based on traffic | Dedicated path remains fixed for entire communication  |
| **Bandwidth**     | Dynamically allocated based on traffic             | Guaranteed bandwidth for the communication             |
| **Efficiency**    | More efficient for bursty data traffic             | Less efficient for bursty data traffic                 |
| **Cost**          | Generally considered more cost-effective           | Can be more expensive, especially for unused bandwidth |
| **Applications**  | Ideal for data transfer (web browsing, email)      | Ideal for real-time communication                      |

#### TCP vs UDP

**TCP**

* Uses three-way handshake to establish a reliable connection
* More reliable than UDP (User Datagram Protocol) but slower in general.
* Used in HTTP, HTTPS, FTP, SMTP, etc.

**UDP**

* Connectionless, efficient but unreliable transmission of packets
* If any packets are lost, they are lost forever
* Typically used for video streaming which uses VoIP (Voice over IP) where efficiency is required

#### HTTP vs HTTPS

* HTTP uses port $80$ while HTTPS uses port $443$ with TCP.
* The main difference between HTTP and HTTPS is that HTTPS uses TLS (Transpoint Layer Security) encryption.

### Applications

* FTP is for uploading, downloading, renaming, deleting, and managing files.
* Used in HTTP, HTTPS, FTP, SMTP, etc.
* Typically used for video streaming which uses VoIP (Voice over IP) where efficiency is required
* Ideal for data transfer (web browsing, email)
* Ideal for real-time communication

---

## 3. Data Management

### Definitions

**Data lifestyle**

The data life cycle refers to the entire period of time that data exists in the system. This life cycle encompasses all the stages that the data goes through, from its creation to its eventual disposal, encompassing the entire lifespan of data within an organisation or system.

**Data Integrity**

Data integrity refers to the accuracy and validity of data.

**Backup**

Backing up means making a copy of the data and storing it on a different storage device.

**Archive**

Data archival refers to the process of identifying, organising and storing data in a secure and accountable manner.

This purpose is to preserve valuable information for legal, regulatory, historical or business purposes while ensuring efficient use of storage resources.

**Version Control**

Version control is defined as a system that tracks the progress of code across the software development lifecycle and its multiplier iterations - which maintains a record of every change complete with authorship, timestamp, and other details - and also aids in managing change.

**File Naming Convention (FNC)**

File naming convention is essentially a framework for naming files in a way that describes what they contain and how they relate to other files.

**Personal Data**

Personal data refers to data about an individual who can be identified from that data, or from that data and other information to which the organisation has or is likely to have access.

**Personal Data Protection Act (PDPA)**

The Personal Data Protection Act (PDPA) is a data protection law comprising various rules that govern the collection, use, disclosure and care of personal data.

It recognises both the rights of individuals to protect their personal data, including rights of access and correction, as well as the needs of organisations to collect, use or disclose personal data for legitimate and reasonable purposes.

### Advantages / Significance

**Version Control**

* Software development includes the continuous process of modifying programs and the version control system makes this task easier.
* It helps developers to store different versions of software safely and in an organised manner.
* You can restore older versions of a life effectively through the use of version control systems.
* Programmers and developers can easily collaborate on a project through the version control system.

**File Naming Convention**

* This helps to minimise the chances of files being misplaced or lost unintentionally due to poor organisation of files.
* Such a convention also enables users to locate files quickly

### Differences

#### Archive vs backup

| Backup                                                                    | Archive                                                             |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| Enables rapid recovery of live, changing data                             | Stores unchanging data no longer in use but must still be retained. |
| One of multiple copies of data                                            | Usually the only remaining copy of data                             |
| Access to data must be quick to show rapid restoration of data            | Speech of access to the data is usually not crucial                 |
| Short term retention of data only for the period when the data is in use. | Long term retention of data for the required period or indefinitely |
| Duplicate copies are periodically overwritten                             | Data should not be altered or deleted.                              |

### Applications

**Archive**

* Regulatory Compliance
* Litigation and e-Discovery
* Historical Analysis
* Disaster Recovery

**Version Control**

* Easy Modification of the codebase
* Reverting Errors
* Collaboration

---

## 4. Data Representation

### Applications

* Binary to Denary
* Denary to Binary
* Denary to Hexi
* Hexi to Denary

---

## 5. Data Validation and Verification

### Definitions

**Data Validation**

Data validation is a process of ensuring that the input data supplied to a system satisfies a set of rules such that it is sensible, complete, and within acceptable boundaries.

Its purpose is to avoid data errors. It does not guarantee that data is accurate.

**Data Verification**

Verification is the process of getting the user to confirm that the data entered was what was intended to be entered.

Essentially, it is a way of preventing errors when data is copied from one medium to another. It does not check if the data makes sense or is within acceptable boundaries. It only checks that the data entered is identical to the original source.

### Differences

* Verification only checks the data is copied correctly
* Validation checks are carries out automatically by the computer
* Verification does not check if data is reasonable / sensible

### Applications

**Validation Checks**

* Presence check
* Type check
* Existence check
* Length check
* Range check
* Format check / Picture check
* Check Digit
* Integrity check
* Lookup checks
* Batch header check

**Test Data**

| Type                               | Description                                                           |
| ---------------------------------- | --------------------------------------------------------------------- |
| **Normal / valid**                 | Typical data values that are valid and will be accepted by the system |
| **Abnormal / invalid / erroneous** | Data values that the system should not accept or should be rejected   |
| **Extreme / boundary**             | Data values that are at the extreme ends of the valid range           |

---

## 6. Encoding

### Definitions / Characteristics

**ASCII code**

* $7$ bits ($128$ characters)
* Extended ASCII: $8$ bits ($256$ characters)

**Unicode**

* Either $8$, $16$ or $32$ bits (UTF-$8$, UTF-$16$, UTF-$32$)
* Capable of encoding a maximum of $1,114,112$ characters
* Currently, as of Unicode version $17.0$, there are $297,334$ assigned characters with code points

### Advantage of Unicode over ASCII code

* Uses less storage

### Disadvantage of Unicode over ASCII code

* Supports many more characters
* Reduces encoding problems

---

## 7. Ethics

### Definitions

**Ethics**

Ethics is a set of rules of behaviour based on ideas of what is morally good and bad and what is morally right and wrong.

**Ethical issues**

Ethical issues involve examining the moral dilemmas and ethical considerations arising from the use of computing and technology such as data privacy and security, surveillance, intellectual property rights (e.g., copyright, patents), digital rights management, ethical considerations in artificial intelligence and machine learning algorithms, and the ethical implications of emerging technologies like biometrics and autonomous systems.

**Legal Issues**

Legal issues are issues where a law has been passed by a government.

### Applications

**The Professionalism of Computing Professionals**

* act at all times with integrity
* accept full responsibility for their work
* always aim to increase their competence
* act with professionalism to enhance the prestige of the profession and the Society

**Copyright Act**

* Copyright Act strengthens creators' and performers' rights by granting default ownership of certain commissioned works to creators and performers, unless stated otherwise in the contract.
* Additionally, it mandates clear identification of creators or performers when using or distributing their works in public, including on online platforms.

**Computer Misuse Act**

* The Computer Misuse Act aims to protect computer material against unauthorized access or modification and prevent abuse of the national digital identity service.
* The Act prohibits unauthorized interception of computer functions and provides penalties for such offenses.

---

## 8. File

### Definitions

**Serial File**

Serial files contain records which have no defined order. Specifically, they are stored in chronological order, that is, as each record is received it is stored in the next available storage position.

**Sequential Files**

Sequential files are serial files whose records are sorted in ascending or descending on a particular key field.

**Absolute Path**

Absolute file paths are the exact file location in the computer or server.

**Relative Path**

Relative file path points to the location of the file in the root folder of an individual web project with reference to the current working file.

### Differences

**Serial File**

* records are in no particular order
* to retrieve a single record, the whole file needs to be read from beginning to end

**Sequential Files**

* records are sorted in ascending or descending on a particular key field
* They are the types of files suited to long term storage of data.
* a particular record is found sequentially reading the value of the key field until the required value is found.

### Applications

* An example of a serial file would be a bank’s records of transactions.
* We usually use this in our coding and programming projects.

---

## 9. Linked List

### Definitions

* A linked list is a dynamic data structure consisting of nodes.
* Each node contains:

  * Data.
  * Pointer to the next node.

**Free Space List**

* Stores unused nodes.
* The free pointer points to the first available node.

### Limitations

* If the free pointer is `NULL`, the free list is empty and insertion cannot proceed (memory overflow).

### Applications

* Ordered Insertion
* Deletion

---

## 10. Misc

### Applications

**Dictionary**

* Traverse a dictionary
* `len(d) # return the number of entries`
* `d.clear() # remove all keys`
* `list(d.values()) # all the values of d in list`
* `list(d.keys()) #all the keys of d in list`

**datetime**

* Current time
* Only show hours, minutes and seconds
* Create an object of a specific time
* Time difference

**csv**

* csvreader
* csvwriter

**random**

* `number = random.randint(1, 10)`

---

## 11. Modularisation

### Definitions

**Modular Programming**

A module can be defined as a section of an algorithm that can be reused and that is dedicated to performing a single function.

* Each module performs a distinct function and has a clearly defined interface for communication with other modules.
* Modules are usually implemented as functions, classes, or separate files
* Promotes reusability, maintainability, readability, and collaboration in software development

**Procedure**

A procedure is a block of program code statements designed to carry out a definable task.

**Function**

A function is a block of program code statements that returns a single value to the program that called it.

### Advantages

* Allow the subroutine to be called from many / multiple places
* May be (independently) tested and debugged
* Reduce unnecessary duplication / programme lines
* Reusability → A module can be reused in different programs
* Maintainability → Easier to update/debug a specific part of the program without affecting others

### Differences

**Procedure vs Function**

* A function only accepts input parameters (pass by values) whereas a procedure accepts input or output parameters (pass by reference)
* A procedure is a bundle of code, it does not have return type whereas function has return type.
* Hence a function may return a value for its input parameters whereas a procedure may not return a value for its input parameters.

**Passing parameters**

* By value: the actual value is passed into the procedure
* By reference: the address of the variable is passed into the procedure

**Global variables vs Local variables**

A global variable exists throughout the entire programme, while a local variable only exists in the subroutine in which it is declared.

---

## 12. Network Security

### Definitions

**Social Engineering Attack**

A social engineering attack is a type of attack that uses deception and trickery to convince unsuspecting users to provide sensitive data or to violate security guidelines.

**Malware**

Malware is malicious code that is designed to gain unauthorised access to, make unauthorised use of, or damage computing devices and networks.

**Firewall**

* A firewall acts as a filter that monitors access between an organisation’s internal network and the Internet at large, allowing some packets to pass and blocking others.
* A firewall allows a network administrator to control access between the outside world and resources within the administered network by managing the traffic flow to and from these resources.

**IDS and IPS**

* IPS is a device that filters out suspicious traffic.
* IDS is a device that generates alerts when it observes potentially malicious traffic.

**Encryption**

Encryption is a process that uses an algorithm and a key to code a message written in plain text into ciphertext, which is transmitted to the recipient.

Decryption is decoding the ciphertext back into the original plain text using a decryption algorithm and a key.

**Symmetric key encryption**

In symmetric key encryption, there is just one key. This key is a secret shared by the sender and the receiver of a message.

**Asymmetric encryption**

Asymmetric encryption, also known as public-key encryption, is a type of encryption that uses a pair of keys to encrypt and decrypt data.

**Digital signature**

It is a cryptographic technique to indicate the owner or creator of a resource or to signify one’s agreement with a document’s content in a digital world.

**Authentication**

End-point authentication is the process of one entity proving its identity to another entity over a computer network, for example, a user proving its identity to an e-mail server.

### Advantages

**Cloud-based firewalls**

* One benefit of cloud-based firewalls is that they can grow with your organisation and, similar to hardware firewalls, do well with perimeter security (preventing unauthorised users from accessing a network).

**Anomaly-based IDS**

* They don’t rely on previous knowledge about existing attacks—that is, they can potentially detect new, undocumented attacks

**Asymmetric encryption over symmetric encryption**

* It eliminates the need to exchange secret keys, which can be a challenging process, especially when communicating with multiple parties.

### Limitations

**Network-based firewall**

* A network-based firewall cannot protect one computer from another on the same network, or any computer from itself.

**Firewalls**

* They cannot protect against attacks from a source if a user has explicitly allowed it to bypass the firewall.
* They also cannot protect against internal attacks since the malicious traffic may not need to pass through a firewall.

**Signature-based IDS**

* They require previous knowledge of the attack to generate an accurate signature.
* A signature-based IDS is completely blind to new attacks that have yet to be recorded.
* Because every packet must be compared with an extensive collection of signatures, the IDS can become overwhelmed with processing and actually fail to detect many malicious packets.

**Anomaly-based IDS**

* It is an extremely challenging problem to distinguish between normal traffic and statistically unusual traffic.

**Symmetric key encryption**

* The issue with symmetric key encryption is delivery of the secret key.

**Digital signature**

* one concern with signing data by encryption is that encryption and decryption are computationally expensive

### Applications

**Types of Social Engineering Attacks**

* Spoofing
* Impersonation
* Phishing
* Pharming
* Vishing / Voice Phishing
* Spear Phishing
* Whaling
* Spam
* Spim
* Hoax

**Malware Attacks**

* Virus
* Worm
* Trojan horse
* Logic Bomb
* Spyware
* Adware
* Rootkit
* Botnet

**Authentication**

* passwords
* biometrics, for example: fingerprints, facial recognition, iris scans
* token values, such as from a physical device, a mobile phone or a software application
* Some applications use two-factor authentication (2FA), which uses two different ways of authentication for better security

---

## 13. Non-relational Database

### Definitions

**CRUD**

* C → Create
* R → Read
* U → Update
* D → Delete

**ACID**

ACID stands for **Atomicity, Consistency, Isolation, and Durability.**

**Atomicity**

* either every operation succeeds or none of them do

**Consistency**

* consistent with any database constraints

**Isolation**

* make sure that all transactions are run in an isolated environment without interfering with each other

**Durability**

* changes in that transaction are written into the database
* data changes are persisted

### Advantages of NoSQL

| Feature                | Description                                                                                                                                                                                                         |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Flexibility**        | Having a flexible data model also means NoSQL databases can address large volumes of rapidly changing data, making them great for agile development, quick iterations, and frequent code pushes.                    |
| **Cost-effectiveness** | NoSQL databases are typically designed to scale out horizontally by using distributed clusters of hardware, as opposed to scaling up by adding expensive and robust servers.                                        |
| **Fast queries**       | Queries in NoSQL databases can be faster than SQL databases.                                                                                                                                                        |
| **Replication**        | NoSQL replication functionality copies and stores data across multiple servers. This replication provides data reliability, ensuring access during downtime and protecting against data loss if servers go offline. |

### Differences between NoSQL and SQL

| Feature              | Relational databases                                                                    | NoSQL databases                                                                  |
| -------------------- | --------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| **Language**         | Use structured query languages to perform operations                                    | Use a dynamic schema to query data.                                              |
| **Data Schema**      | Have a predefined and fixed format, which cannot be changed for new data.               | NoSQL databases are more flexible.                                               |
| **Scalability**      | Is vertically scalable                                                                  | horizontally scalable                                                            |
| **Big Data Support** | The vertical scaling makes it difficult for relational databases to store very big data | The horizontal scaling and dynamic data schema make NoSQL suitable for big data. |
| **Properties**       | Use the ACID (Atomicity, Consistency, Isolation, Durability) property.                  | Settles for eventual consistency                                                 |

### Applications

**NoSQL databases**

* Social Media
* Logistics and Supply Chain
* Gaming

**SQL databases**

* Finance
* Retail
* Government and Public Sector

---

## 14. OOP

### Definitions

**Procedure**

Writing programs made of functions that perform specific tasks

**Object-Oriented Programming**

focused on creating objects

Object: entity that contains data and procedures

**Class**

Blueprint for creating objects. Defines attributes (data) and methods (behavior).

**Object**

An instance of a class. Represents a real-world entity with state (attributes) and behavior (methods).

**Abstract Data Type (ADT)**

A conceptual model that defines a set of operations and behaviours for a data structure, without specifying how these operations are implemented or how data is organised in memory

**Constructor**

A constructor is a method that is automatically called when an object is instantiated.

**Destructor**

A destructor is a method that is invoked when the object is going to be destroyed.

### Advantages

**Encapsulation**

* Restricts direct access to internal data (e.g., using private attributes).
* Separates interface (what the class exposes) from implementation (internal details).
* Provides controlled access via public methods (getters/setters).
* This reduces accidental errors as programmers cannot change the attribute directly which may lead to an inconsistent state.

**Abstraction**

* Promotes modularity and reduces dependency on implementation details.

**Inheritance**

* Reduces code duplication, promotes reusability, specialization and extendability.

**Polymorphism**

* Reduces complexity by allowing one interface, multiple behaviors.

### Applications

**4 Pillars of OOP**

* Encapsulation
* Abstraction
* Inheritance
* Polymorphism

---

## 15. Program Memory Allocation

### Purpose / Applications

**Code Segment (CS) or Text Segment**

* Stores all the executable instructions (machine code) of the program
* Complied code of functions and methods
* Constants such as string literals in some systems

**Data Segment (DS) / Initialised Data**

* Stores all global and static variables that have been explicitly initialised before execution begins.

**BSS (Block Started by Symbol)**

* Stores global and static variables that are declared but not initialised (uninitialised data).

**Heap / Extra Segment (ES)**

* Used for dynamic memory allocation during program execution (runtime)

**Stack Segment (SS)**

* Used for function call management and storing temporary variables
* Function parameters
* Return addresses
* Local variables

### Advantages of using dynamic ds over static ds

* Flexible size

  * Can grow or shrink during program execution. No need to know the size beforehand.
* Better memory utilisation

  * Memory is allocated only when needed, reducing wasted space.

### Disadvantages of using dynamic ds over static ds

* More memory overhead

  * Slower access
* Many dynamic structures (e.g., linked lists) do not support direct indexing, so elements may need to be traversed one by one.

---

## 16. Queue

### Definitions

**Linear Queue**

* A FIFO (First In, First Out) data structure.
* Insertion occurs at the rear.
* Deletion occurs at the front.

**Circular Queue**

* Treats the array as circular.
* Next position: `(pointer + 1) % maxsize`

**Priority Queue (Heap)**

* Removes elements according to priority rather than insertion order.

### Advantages

**Circular Queue**

* Reuses empty spaces.
* Better memory utilisation.
* Supports continuous insertion and deletion.
* Maintains FIFO order.

### Limitations

**Linear Queue**

Freed spaces at the front cannot be reused once RP reaches the end.

### Applications

* Printer queues.
* CPU scheduling.
* Keyboard buffering.
* Network packet buffering.
* Breadth-First Search (BFS).
* Producer-consumer systems.
* I/O buffering between CPU and peripherals.

---

## 17. Recursion

### Definition

* A recursive function is a function that calls itself (#1).
* The recursive function must have a base case (#2),
* and it must change its state and move toward the base case (#3).

### Advantages

* Sometimes, recursive solutions are shorter than non-recursive ones
* When the solution to be problem is essentially recursive (e.g. DFS)

### Limitations

* May require large amounts of memory if the depth of recursion if large

  * Could result in stack overflow, causing the program to crash
  * Memory overheads of stack use with many recursive procedural calls
* Recursive routines are sometimes very slow in execution owing to the overheads in memory involved in repeatedly calling the subroutine and storing and retrieving return addresses and parameters
* Recursive routines can be difficult to follow and to debug

---

## 18. Relational Databases

### Definitions

**Super key**

A super key is a set of attributes that uniquely identifies any row in a table. The set is **not necessarily minimal**.

**Candidate key**

A candidate key is a minimal set of attributes that uniquely identifies any row in a table.

**Primary key**

A primary key is a candidate key that is chosen by the database designer to uniquely identify any row in a table.

**Secondary key**

A secondary key is a candidate key that is not a primary key.

**Prime attribute**

A prime attribute is an attribute that is **part of at least one candidate key**.

**Functional Dependency**

`X → Y`

Means that Y is dependent on X.

**Transitive Dependency**

An attribute Z is said to be transitively dependent on X if X → Y and Y → Z.

**Data Redundancy**

Refers to data being stored more than once.

**Database Normalisation**

Database Normalisation is the process of structuring a relational database to reduce **data redundancy** and improve data integrity

### Limitations / Issues with data redundancy

| Problem                    | Description                                                                                                    |
| -------------------------- | -------------------------------------------------------------------------------------------------------------- |
| **Insertion Anomaly**      | Occurs when you cannot insert new data into the table without inserting unrelated or unnecessary data.         |
| **Updating Anomaly**       | Occurs when updating data requires multiple rows, and failing to update all of them causes data inconsistency. |
| **Deletion Anomaly**       | Occurs when deleting a row unintentionally deletes important data.                                             |
| **Storage Requirements**   | More data is required to store duplicate values if there is redundant data.                                    |
| **Maintenance Complexity** | Multiple copies of the same data has to be updated/inserted/deleted, increasing maintenance complexity.        |

### Differences / Normal Forms

**1NF**

* All fields must be **atomic**
* There should be no repeating groups/arrays in a single row

**2NF**

* Must be 1NF
* Every non-key attribute must depend on the whole primary key, not just part of it

**3NF**

* Must be 2NF
* There are no transitive dependences

**BCNF**

* Must be 3NF
* For every functional dependency X → Y, X must be a **candidate key**.

### Applications

* Select Query
* Update Query
* Insert Query
* Delete Query
* Drop Table Query
* Create Table Query
* ER (Entity Relationship) Diagram

---

## 19. Searching Algorithm

### Definitions

**Hash Table**

* A hash table stores key-value pairs.
* A hash function converts a key into an array index for fast storage and retrieval.

### Differences

**Linear Search**

* Best Case: $O(1)$
* Average Case: $O(N)$
* Worst Case: $O(N^2)$

**Binary Search**

* Best case: $O(1)$
* Average Case: $O(logN)$
* Worst Case: $O(logN)$

**Linear Probing**

* Consecutive slots.
* More clustering.
* Covers the whole table.

**Quadratic Probing**

* Squared jumps.
* Less clustering.
* May not cover the whole table.

**Chaining**

* Each hash table index stores a linked list.
* Colliding keys are stored in the same linked list.
* Faster insertion.
* Easier deletion.
* Smaller table acceptable.
* Long chains reduce performance.

### Applications

* Database indexing.
* Password hashing/encryption.
* Dictionaries (Maps).
* Caching.

### Characteristics of a Good Hash Function

* The same key always produces the same hash value.
* Uniform distribution of hash values.
* Minimises collisions and clustering.
* Uses all parts of the key.
* Fast to compute.

---

## 20. Sorting Algorithm

### Differences

**Bubble Sort**

* Worst-Case: $O(N^2)$
* Avg-Case: $O(N^2)$
* Best Case: $O(N)$

**Insertion**

* Best for small size arrays
* Time complexity of $O(n^2)$

**Quick Sort**

* Best case: $O(Nlog_2N)$
* Average case: $O(Nlog2N)$
* Worse case: $O(N^2)$
* If the list is completely or almost ordered, it can take a running time of order $N^2$.

**Merge Sort**

* Worst Case Time: $O(Nlog_2N)$
* Best Case Time: $O(Nlog_2N)$
* Average Time: $O(Nlog_2N)$
* Not recommended for large unsorted arrays as it requires equal amount of additional space as the unsorted array.

### In-place vs Not-In-place

**In-place sort**

* Performed when the number of elements is small enough to fit into the main memory.
* To produce the desired output, modification to the data set only requires only small and constant extra space.
* Insertion sort, bubble sort, quick sort

**Not-In-place sort**

* When all elements that needs to be sorted cannot be placed in memory at a time, therefore additional memory is required to perform the sorting
* Merge sort

### Advantages / Limitations

* Bubble sort does perform better for partially sorted lists because it is able to detect when a list is sorted and does not continue making unnecessary passes through the list.
* As a general sorting scheme, however, it is very inefficient because of the large number of interchanges that it requires.
* Insertion sort also is too inefficient to be used as a general-purpose sorting scheme. However, the low overhead that it requires makes it better than bubble sort.
* While Quick sort partitions and usually makes less comparisons than Bubble sort and Insertion sort, in the worst case scenario the time complexity is still $O(n^2)$.
* Merge sort has a time complexity of $O(nlog_n)$ and is a very efficient general-purpose sorting schemes and especially for large lists.

---

## 21. Stack

### Definition

A stack is a linear data structure that stores elements in a Last In, First Out (LIFO) order, meaning the last element added (pushed) is the first one removed (popped).

### Characteristics

* Order: Last In, First Out (LIFO)
* Access: Only the top element is directly accessable
* Dynamic Size: Can grow or shrink as elements are pushed or popped
* Restricted Operations: Unlike arrays/lists, you can’t directly access elements by index directly
* Implementation: Can be implemented using arrays (static stack) or linked lists (dynamic stack)

### Applications

* `push(x)` – adds element x at the top of the stack
* `pop()` – removes and returns the element from the top of the stack
* `peek() or top()` – returns the topmost element without removing it
* `isEmpty()` – checks whether the stack is empty
* `isFull()` – (for fixed stacks) checks if the stack has reached its max size

---

## 22. Tree

### Definition

* A hierarchical data structure consisting of nodes.
* Each node is linked to one or more nodes below it.

### Applications

**Preorder (Root → Left → Right)**

* Visit the `root`
* Traverse the `left` subtree.
* Traverse the `right` subtree.

**Inorder (Left → Root → Right)**

* Traverse the `left` subtree.
* Visit the `root`.
* Traverse the `right` subtree.
* For a Binary Search Tree (BST), this traversal visits nodes in ascending order.

**Postorder (Left → Right → Root)**

* Traverse the `left` subtree.
* Traverse the `right` subtree.
* Visit the `root`.

**Binary Search Tree (BST) Search**

* Accept the data to search.
* Start from the root.
* While the current node is not NULL:

  * If `data == current node`, print "Found" and stop.
  * If `data < current node`, move to the left subtree.
* Else, move to the right subtree.
* If `NULL` is reached, print "Not Found".

---

## 23. Web Applications

### Definitions

**Native apps**

* An executable program coded in the machine language of the hardware platform it is running in.

**Web apps**

* An application in which all or some parts of the software are downloaded from the Web every time it runs.

**Browser-Based**

* A browser-based web app is an application built with web technologies (typically HTML, CSS, and JavaScript) that users access through a web browser over the internet or a local network, without requiring installation from an app store.

**Client-Based**

* A client-based application is software installed on a user's device that executes locally, without a browser, and may communicate with remote servers or services to access data, synchronize information, or perform network-based functions

### Advantages

**Native apps**

* Optimum access to device hardware and features.
* Potential for high performance and high responsiveness.
* Enhanced user experience.
* Offline capabilities

**Web apps**

* Cross-Platform Compatibility
* No requirements for installation
* Update and app maintenance.
* Cost-effective development
* Greater discoverability

### Limitations

**Native apps**

* App store approval
* Longer development time and costs
* Limited distribution and discoverability outside the app store.
* Fragmentation and compatibility challengers.

**Web apps**

* Internet Connectivity Dependency
* Limited device feature access
* Performance constraints.
* Security considerations

### Differences

| Feature                        | Web Applications                                                                                                                     | Native Applications / Desktop Applications                                                                                    |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------- |
| **Deployment and Maintenance** | Deployment and maintenance (updates) for a web-based application require deployment on a single set of server machines.              | Deployment and any maintenance/patch are done on individual client machines separately.                                       |
| **Accessibility**              | Web applications can be accessed from anywhere (most locations), so there is no location constraint.                                 | As desktop are confined to a standalone machine, so they can be only accessed from the machines they are deployed in.         |
| **Platform Compatibility**     | Web applications are platform-independent, they can work in different types of platforms with the only requirement of a web browser. | Desktop applications need to be developed separately for different platform machines.                                         |
| **Security**                   | Web applications are at higher security risks as they are inherently designed to increase accessibility.                             | Desktop applications, on the other hand, have better authorization and administrators have better control, hence more secure. |
| **Internet Connectivity**      | Web applications rely heavily on internet connectivity, for their operation.                                                         | Desktop applications don’t require the internet for their operations.                                                         |

### Applications

**Quality of a web application**

* Learnability
* Efficiency
* Memorability
* Errors
* Satisfaction

**Nielsen’s 10 principles**

* Visibility of system status
* Match between system and the real world.
* User control and freedom
* Consistency and standards
* Error prevention
* Recognition rather than recall
* Flexibility and efficiency of use
* Aesthetic and minimalist design
* Help users recognise, diagnose and recover from errors
* Help and documentation

**Web development**

* CSS
* Flask
* Templates
* Jinja2
* Static Files
* Processing Form Data
* Handling File and Image Uploads
* Socket Programming
