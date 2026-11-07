---
tags:
  - network
  - security
---

## What is Network Security?

Network Security → The shield that protects the CIA of information and resources in a network.

## CIA Triad

| Principle       | Description                                                                                                                                                    |
| --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Confidentiality | Ensuring only authorized users can access sensitive information within a network using encryption and access controls.                                         |
| Integrity       | Ensuring data within a network is accurate and has not been tampered with using intrusion detection systems.                                                   |
| Availability    | Ensures that authorized users can access the information and resources they need whenever they require them using firewalls and network redundancy strategies. |

Original wording preserved, with key concepts highlighted.




# Malmares

## Social Engineering Attacks

### Definition

A social engineering attack is a type of attack that uses deception and trickery to convince unsuspecting users to provide sensitive data or to violate security guidelines.

### Types of Social Engineering Attacks

| Type | Description |
|---|---|
| **Spoofing** | This is a human- or software-based attack in which the goal is to pretend to be someone else for the purpose of concealing their identity.<br><br>Spoofing can occur through:<br><br>- Using IP addresses (IP spoofing)<br>- A network adapter’s hardware media access control (MAC) addresses (MAC Spoofing)<br>- Email. Various email message headers are changed to conceal the originator’s identity. |
| **Impersonation** | This is a human-based attack in which an attacker pretends to be someone he’s not.<br><br>A common scenario is when the attacker calls an employee and pretends to be calling from the help desk. The attacker tells the employee he is reprogramming the order-entry database, and he needs the employee’s user name and password to make sure it gets entered into the new system. |
| **Phishing** | Email-based social engineering attack<br><br>In a phishing attack, the attacker sends an email message that seems to come from a respected bank or other financial institution. The message claims that the recipient needs to provide an account number, Social Security number, or other private information to the sender in order to “verify an account”. |
| **Pharming** | A cyber-attack that redirects users to fraudulent websites or manipulates their computer systems to collect sensitive information. Victims are tricked into thinking that these fraudulent websites are legitimate. |
| **Vishing / Voice Phishing** | This is a human-based attack for which the goal is to extract personal, financial, or confidential information from the victim by using services such as the telephone system and IP-based voice messaging services such as VoIP as the communication medium.<br><br>The term “vishing” is the shortened form of “voice phishing”. |
| **Spear Phishing** | This form of phishing targets specific individuals, employees or mid-level staff across an organisation to steal general credentials or access. |
| **Whaling** | This is a form of spear phishing that targets individuals who are known to be upper-level executives or other high-profile employees.<br><br>Whaling attacks are well-researched attempts to access sensitive information and often resemble a legal subpoena, customer complaint, or executive issue. The content is meant to be tailored for upper management, and usually involves an alleged company-wide concern. Like phishing messages, spear phishing / whaling attacks try to convince the target to access malicious content such as hyperlink, file, or attachment. |
| **Spam** | Spam is an email-based threat in which the user’s inbox is flooded with email messages that act as vehicles carrying advertising material for products or promotions for get-rich-quick schemes and can sometimes deliver viruses or malware. |
| **Spim** | Spim is an IM-based attack similar to spam that is propagated through instant messaging instead of through email.<br><br>Spim → **Sp**am over **i**nstant **m**essaging. |
| **Hoax** | A false message or warning about a non-existent computer virus, security threat or cyber incident. They trick people into panic, wasting time, and forwarding the fake warning to others.<br><br>Two things may happen:<br><br>1. Hoax is disseminated, clogging up communication systems, and possibly triggering a Denial of Service (DoS) condition.<br>2. Users react by following instructions in the hoax that direct them to defend or secure their devices in an improper or unapproved manner. |



### Malware Attacks

Malware is malicious code that is designed to gain unauthorised access to, make unauthorised use of, or damage computing devices and networks.

| Type | Description |
|---|---|
| **Virus** | A sample code that spreads from one computer to another by attaching itself to other files. The code in a virus executes when the file it is attached to is opened.<br><br>Frequently, viruses are intended to enable further attacks, send data back to the attacker, or even corrupt or destroy data. |
| **Worm** | A piece of code that spreads from one device to another on its own, not by attaching itself to another file. Like a virus, a worm can enable further attacks, transmit data, or corrupt and erase files. |
| **Trojan horse** | An insidious type of malware that is itself a software attack and can pave the way for a number of other types of attacks. There is a social engineering component to a Trojan horse attack because the user has to be fooled into executing it. |
| **Logic Bomb** | A piece of code that sits dormant on a target device until it is triggered by a specific event, such as a specific date. Once the code is triggered, the bomb “detonates”, and performs whatever actions it was programmed to do. Often, this includes erasing and corrupting data on the target device. |
| **Spyware** | Surreptitiously installed malicious software that is intended to track and report on the usage of a target device, or collect other data the author wishes to obtain.<br><br>Data collected can include web browsing history, personal information, banking and other financial information, and usernames and passwords |
| **Adware** | Software that automatically displays or downloads advertisements when it is used. While not all adware is malicious, many adware programs have been associated with spyware and other types of malicious software. Also, it can reduce user productivity by slowing down devices and simply by creating annoyances. |
| **Rootkit** | Code that is intended to take full or partial control of a device at the lowest levels.<br><br>Rootkits often attempt to hide themselves from monitoring and detection, and modify low-level system files when integrating themselves into a device. Rootkits can be used for non-malicious purposes such as virtualisation; however, most rootkit infections install backdoors, spyware, or other malicious code once they have control of the target device. |
| **Botnet** | A set of devices that have been infected by a control program called a bot that enables attackers to exploit them and mount attacks. Typically, black hats use botnets for Distributed Denial of Service, or DDoS attacks, sending spam email, and mining for personal information or passwords. |



### Types of Viruses

| Type                       | Description                                                                                                                                                                                                                                                                                                                                                                                          |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Boot Sector**            | Infects any disk-based media. Writes itself into the boot sector of the disk. When a system attempts to boot from the disk, the virus is moved onto the system. Once on the system, the virus attempts to move itself to every disk placed in the system.                                                                                                                                            |
| **Macro**                  | A macro is a group of application-specific instructions that execute within a specific application, A macro virus uses other programmes’ macro engines to propagate. True macro viruses do not actually infect files or data, but attach themselves to the file’s template, document or macro code. Microsoft Office products have been popular targets for macro viruses.                           |
| **Mailer and mass mailer** | A mailer virus sends itself to other users through the email system. It simply rides along with any email that is sent.<br><br>A mass mailer virus searches the email system for mailing lists and sends itself to all users on the list.<br><br>Often, the virus does not have a payload; its purpose is to disrupt the email system by swapping it with mail messages in the form of a DOS attack. |
| **Polymorphic**            | The type of virus changes as it moves around, acting differently on different systems. It can sometimes even change the virus code, making it harder to detect                                                                                                                                                                                                                                       |
| **Script**                 | A small program that runs code by using the Windows scripting host on Windows operating systems.<br><br>It is written as a script in Visual Basic or Javascript and executes when the script runs. Scripts are often distributed by email and requires use to open them                                                                                                                              |
| **Stealth**                | A stealth virus moves and attempts to conceal itself until it can propagate. After that, it drops its payload.                                                                                                                                                                                                                                                                                       |

### The difference between a Trojan horse and a worm
Trojan: Masquerades as legitimate software and tricks users to execute it, does not replicate itself
Worm: Self-replicating, spreads autonomously through networks




# Firewalls

Firewall monitors and controls all incoming and outgoing network traffic based on a set of security rules to prevent unauthorized access from entering a private network.  

### Limitations:
Hackers can bypass firewall by inserting malicious attacks inside legitimate programs, for example, emails
Firewall cannot protect against internal attacks, for example, virus in one computer in the network
The setting of firewall may block some legitimate programs


## 1. Types of Firewalls

| Type                   | Description                                                                                                                  |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| Hardware Firewall      | Physical, connects the network and gateway through wires                                                                     |
| Software Firewall      | Internal, works using port numbers and applications                                                                          |
| Cloud-based Firewall   | Firewalls can grow with the organization and do well with perimeter security                                                 |
| Host Based Firewall    | Installed on an individual computer to protect it from activity occurring on its network                                     |
| Network Based Firewall | May be installed at the perimeter of a network to protect corporations from hosts on the internet, cannot protect internally |

## 2. Functionality of Firewalls

| Functionality        | Description                                                                                                                                       |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| Traffic Control      | All communication must pass through the firewall. Using a single firewall helps ensure this, but bigger organizations may enforce multiple layers |
| Authorized Traffic   | Only authorized traffic will be allowed to pass, and the rest are blocked                                                                         |
| Maintaining Security | While connected to the network itself the firewall is meant to be resistant to attacks                                                            |

## 3. Applications of Firewalls

| Application             | Description                                                                                                                                               |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Packet Filters          | Occur at gateway routers that connect internal networks to ISPs. The admins can specify what’s allowed and what is not.                                   |
| Stateful Packet Filters | Track TCP connections and use this information to make filtering decisions                                                                                |
| Application Gateways    | Application specific servers through which all app data must pass. They look beyond just IP TCP UDP Headers and make the decisions based on the app data. |

All descriptions preserve the original wording, with line breaks cleaned up for readability.



# Denial of Service (DoS)

- A Distributed Denial-of-Service (DoS) attack is carried out by one or a group cybercriminals that controls a network of Internet-connected machines known as botnet.
- The attacker then sends remote instructions to each bot in the botnet to send voluminous bogus requests to the server that stored the medical records to overwhelm the resource and capacity of the server.
- When the server direct its resources to handle the bogus requests and gets overwhelmed, it results in depriving the genuine users of the medical system from accessing the information stored in the system.




# Intrusion Detection System and Intrusion Prevention System

- IPS is a device that filters out suspicious traffic.
- IDS is a device that generates alerts when it observes potentially malicious traffic. 

>[!note]
> We will collectively refer to IDS systems and IPS systems as IDS systems.


### IDS

- An IDS can be used to detect a wide range of attacks, including network mapping (emanating, for example, from nmap), port scans, TCP stack scans, DoS bandwidth-flooding attacks, worms, and viruses, OS vulnerability attacks, and application vulnerability attacks.

IDS systems are broadly classified as either **signature-based systems** or **anomaly-based systems.**

- Signature Based IDS
	- Requires previous knowledge of attacks to generate accurate signatures
	- Blind to new, undocumented attacks
	- Can produce false alarms even if a signature is matched
	- Every packet must be compared with an extensive collection of signatures
	- Can become overwhelmed and fail to detect many malicious packets

- Anomaly Based IDS
	- Creates a traffic profile based on normal operation
	- Detects statistically unusual packet streams (e.g., high percentage of
	- ICMP packets, exponential growth in port scans and ping sweeps)
	- Can detect new, undocumented attacks
	- Challenging to distinguish between normal and unusual traffic
	- Most IDS deployments are primarily signature-based, with some including anomaly-based features

- HOW IDS WORKS
	- Network is divided into high-security region and DMZ
	- High-security region protected by packet filter and application gateway
	- DMZ includes public web server and DNS server, protected by packet filter
	- IDS sensors monitor both regions
	- IDS performs deep packet inspection and signature comparison
	- Placing IDS sensors downstream reduces traffic load per sensor
	- Signature-based IDS uses a database of attack signatures
	- Signatures are created by network security engineers and can be customized
	- IDS inspects each packet and generates alerts for matches
	- Alerts are sent to administrators, management systems, or logged





# Secure access method

### Encryption

Encryption is a process that uses an algorithm and a key to code a message written in plain text into ciphertext, which is transmitted to the recipient. 

Decryption is decoding the ciphertext back into the original plain text using a decryption algorithm and a key.

##### Purpose

- Encryption is often used to protect data from unauthorised access by allowing only authorised users to have the secret key. 
- It can also be used in combination with file permissions so that an unauthorised user who is able to bypass file permissions would still be unable to use the accessed data without knowing the secret key.

##### Symmetric key encryption

- In symmetric key encryption, there is just one key. This key is a secret shared by the sender and the receiver of a message.

```mermaid
flowchart LR
    A[Plaintext] --> B[Encryption Algorithm]
    K[Shared Secret Key] --> B
    B --> C[Ciphertext]
    C --> D[Decryption Algorithm]
    K --> D
    D --> E[Plaintext]
```

- The sender uses the encryption algorithm together with the key to encrypt some plaintext. The receiver decrypts the ciphertext using the same key
- The issue with symmetric key encryption is delivery of the secret key. The sender needs the key to encrypt but it is difficult to securely deliver the key to the receiver to allow decryption

###### Example

- Examples of old symmetric key cryptography are Caesar cipher, monoalphabetic cipher, polyalphabetic encryption. 
- Modern symmetric key cryptography is categorised into two broad areas - stream ciphers and block ciphers. The latter typically, uses a technique called Cipher Block Chaining (CBC).


##### Asymmetric encryption

- Asymmetric encryption, also known as public-key encryption, is a type of encryption that uses a pair of keys to encrypt and decrypt data.

- The pair of keys includes a public key, which can be shared with anyone, and a private key, which is kept secret by the owner.
	- allows for secure communication between two parties without the need for both parties to have the same secret key.

```mermaid
flowchart LR
    A[Original Plaintext] --> B[Encryption]
    PUB[Recipient's Public Key] --> B
    B --> C[Encrypted Ciphertext]

    C --> D[Decryption]
    PRI[Recipient's Private Key] --> D
    D --> E[Original Plaintext]
```

##### Advantage of asymmetric encryption over symmetric encryption

- It eliminates the need to exchange secret keys, which can be a challenging process, especially when communicating with multiple parties.
	- If asymmetric encryption is to be used, the process is initiated by someone in possession of two keys. One of these is a public key, which is sent to anyone who is going to partake in an encrypted communication. The other is a secret private key, which is never sent to anyone. Having a means of secure transmission of a secret key is no longer an issue.

### Example

- Examples of asymmetric encryption algorithms include Rivest-Shamir-Adleman (RSA), Diffie-Hellman, and Elliptic Curve Cryptography (ECC).





# Digital signature

- It is a cryptographic technique to indicate the owner or creator of a resource or to signify one’s agreement with a document’s content in a digital world. 
- Therefore, it must be possible to prove that a document signed by an individual was indeed signed by that individual (the signature must be verifiable) and that only that individual could have signed the document (the signature cannot be forged).

##### Asymmetric encryption allows for the creation of digital signatures

- Asymmetric encryption allows for the creation of digital signatures, which can be used to verify the authenticity of data. 
- Using asymmetric encryption, the decryption-encryption works if the keys are used the other way round.
- An individual can encrypt a message with a private key and send this to a recipient who has the corresponding public key, who can then use the public key to decrypt the received ciphertext. 
- This approach would not be used if the content of a message was confidential because anyone might be in possession of the public key.
- However, it could be used to verify who the sender was. Only the sender has the private key and the public key only works with that one specific private key
###### Limitation

- one concern with signing data by encryption is that encryption and decryption are computationally expensive

##### Public cryptographic one-way hash function

- Public cryptographic one-way hash function which creates a fixed-length hash that is uniquely defined for the particular message, called a ‘digest’.
	- A one-way function is called a Hash Function → relatively easy to compute the output from the input, but significantly harder in the reverse. 

- At the receiver end, the same public one-way hash function is used to create a digest from the received message. The encrypted version of the original digest is decrypted using the public key. If the two digests are identical, the receiver can be confident that the message is authentic and has been transmitted unaltered.


>[!Procedure of a Digital Signature]
> - Message is hashed and encrypted with sender's private key.
> - This forms the digital signature.
> - Original message is sent with the digital signature.
> - Receiver would decrypt the digital signature with sender's public key to obtain the hashed message
> - The original message is hashed and compared with the hash message in step 3.
> - If the two are identical, the receiver can be certain the message did come from the sender, and hence the message is authenticated. 

###### Sender:

```mermaid
flowchart LR
    A[Message] -->|Hashing| B[Hashed Message]
    B -->|Sender's Private Key| C[Digital Signature]
    C --> D[Digital Signature + Message]
    D --> E[Send to Receiver]
```
###### Receiver:

```mermaid
flowchart LR
    A[Digital Signature] -->|Sender's Public Key| B[Hashed Message]
    C[Message] -->|Hashing| D[Hashed Message]
```
### Limitation 
A digital is a method of ensuring that an encrypted message is from a trusted source as they have a certificate from a Certification Authority that confirms that the individual is who they claim to be in an online communication.However, it is unable to verify the authenticity of message content and whether the message has been tampered with.



# Authentication 

- End-point authentication is the process of one entity proving its identity to another entity over a computer network, for example, a user proving its identity to an e-mail server.
	- For example, a user proving its identity to an e-mail server. A concrete example is a user authenticating him or herself to an e-mail server.

- Often, network elements such as routers and client/server processes must authenticate each other. 
	- Here, authentication must be done solely on the basis of messages and data exchanged as part of an authentication protocol. 
	- Typically, an authentication protocol would run before the two communicating parties run some other protocol. 
	- The authentication protocol first establishes the identities of the parties to each other’s satisfaction; only after authentication do the parties get down to the work at hand. 


>[!Common ways of authentication include:]
>- passwords  
>- biometrics, for example: fingerprints, facial recognition, iris scans 
>-  token values, such as from a physical device, a mobile phone or a software application

- Some applications use two-factor authentication (2FA), which uses two different ways of authentication for better security

### Biometrics authentication

Biometric Authentication Preferred Because:  
1. Unique physiological traits
2. Cannot be lost/stolen like tokens
3. Harder to replicate than token codes
   OR
   Security Tokens Preferred Because:
4. Not affected by physical changes
5. Easier to revoke/reissue
6. No biometric data storage risks
   (Accept either position with valid reasoning)


### How hash protects passwords from leaking 

Since a hash is irreversible, it is impossible to recover the original password from the hashed form. This ensures that even if the server’s database is compromised, it is not possible to recover the list of passwords.
When a user logs in, the password entered by the user is hashed and this is compared to the hashed password stored under the user’s name in the database. If they do not match, then the user has logged in with an incorrect password and will be prompted to retry.



