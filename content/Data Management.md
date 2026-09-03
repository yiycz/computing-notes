---
tags:
  - theory
  - data-management
---
# Data lifestyle

The data life cycle refers to the entire period of time that data exists in the system. This life cycle encompasses all the stages that the data goes through, from its creation to its eventual disposal, encompassing the entire lifespan of data within an organisation or system.

```mermaid
flowchart LR
    A[Creation] --> B[Storage]
    B --> C[Usage]
    C --> D[Archival]
    D --> E[Destruction]
```


# Data Integrity 

Data integrity refers to the accuracy and validity of data.

Can be compromised due to 

| Type of Error | Description |
|---|---|
| **Errors on input** | Data that is keyed in may be wrongly transcribed. A batch of transaction data could go astray, or be keyed in twice by mistake. |
| **Errors in operating procedures** | An update program could for example be run twice in error and quantities on a master file would then be updated twice. |
| **Program errors** | These could lead to corruption of files; a new system may have errors in it that will not surface for some time, or errors may be introduced during program maintenance. |
| **Viruses** | Files can be corrupted or deleted if disk becomes infected with a virus. |
| **Transmission errors** | Interference or noise in a communications link may cause bits to be wrongly received. |


# Need for data security

|Cause|Elaboration|
|---|---|
|Hardware failure|Secondary devices may experience wear and tear over time, reducing reliability and increasing the risk of data loss|
|Human Actions|Humans may accidentally delete or overwrite data. They may also format or partition the wrong drive or handle storage media improperly, leading to data loss|
|Software corruption|Issues with software, operating system failures, or bugs can cause data corruptions or loss. → occurs during updates, installations|
|Power Failures|Sudden power outages or voltage fluctuations can interrupt data transfers or damage storage devices, leading to data loss|
|Theft or loss|If a device containing important data is stolen or lost, the data may be permanently inaccessible.|
|Malware and ransomware|Malicious software can encrypt, delete, or compromise data, making it inaccessible unless a ransom is paid.|
|Viruses and cyber-attacks|Viruses, worms, trojans or other cyber-attacks can corrupt or delete data, compromise system integrity, cause data loss.|
|Software or hardware incompatibility|Using incompatible software or hardware components can lead to data corruption or loss.To mitigate the risk of data loss, it is important to regularly backup important data, implement robust security measures, and use reliable hardware and software.|

## Backup

Backing up means making a copy of the data and storing it on a different storage device.

## Archive

Data archival refers to the process of identifying, organising and storing data in a secure and accountable manner.

This purpose is to preserve valuable information for legal, regulatory, historical or business purposes while ensuring efficient use of storage resources.

|Key considerations|Elaboration|
|---|---|
|Data Classification|Data should be prioritised based on its value, sensitivity, and legal/regulatory requirements to determine the appropriate archival strategy.|
|Retention Policies|The period of retention for the archived data must be based upon legal, industry or organisational requirement, taking into consideration factors like sensitivity and business needs|
|Storage infrastructure|To ensure cost-efficiency, it is important to adopt a scalable and reliable storage system capable of accommodating large volumes of data over extended periods|
|Metadata and indexing|Descriptive metadata and indexing mechanisms can be implemented to facilitate efficient search and retrieval of archived data.|
|Data security|Archived data should be protected against unauthorized access, tampering, and data breaches by implementing appropriate security controls.|
|Data integrity and preservation|Data integrity checks, periodic validation, and migration strategies should present the integrity and usability of archived data over time.|

|Importance of data archival|Elaboration|
|---|---|
|Regulatory Compliance|Archiving data helps organizations meet legal and regulatory requirements, such as data retention periods mandated by industry-specific regulations.|
|Litigation and e-Discovery|Archived data can be crucial in legal proceedings, enabling organizations to retrieve and present evidence when required.|
|Historical Analysis|Archiving data allows for retrospective analysis and trend identification, aiding in strategic decision-making and historical research.|
|Disaster Recovery|While the archived copy of the data may not be the latest backup copy of the data, it can still serve as a backup in the event of data loss or system failures, ensuring business continuity.|

## Archive vs backup

|Backup|Archive|
|---|---|
|Enables rapid recovery of live, changing data|Stores unchanging data no longer in use but must still be retained.|
|One of multiple copies of data|Usually the only remaining copy of data|
|Access to data must be quick to show rapid restoration of data|Speech of access to the data is usually not crucial|
|Short term retention of data only for the period when the data is in use.|Long term retention of data for the required period or indefinitely|
|Duplicate copies are periodically overwritten|Data should not be altered or deleted.|

## Version Control

Version control is defined as a system that tracks the progress of code across the software development lifecycle and its multiplier iterations - which maintains a record of every change complete with authorship, timestamp, and other details - and also aids in managing change.

### Significance

##### Easy Modification of the codebase

- Software development includes the continuous process of modifying programs and the version control system makes this task easier. 
- Version control software is used by software developers to maintain documentation and configuration files as well as source code.
- It helps developers to store different versions of software safely and in an organised manner. 

#####  Reverting Errors

- Version control can be excellent help for emergency hot-fixes, routine maintenance, upgrades and new features with potentially overlapping development timeframes. 
- When you need to troubleshoot an issue, you can easily access and compare the last working life with the faulty file, and decrease the time spent identifying the cause of an issue. 
- You can restore older versions of a life effectively through the use of version control systems. You can simply undo every commit you have done in just a few clicks. 

##### Collaboration

- Programmers and developers can easily collaborate on a project through the version control system. Everyone can access the database simultaneously to view previous versions. It will be easier for them to work simultaneously as a team regardless of their location.
- Version control allows developers to store the history of changes and who made them, enabling them to revert or look back to previous versions of documents and understand how contributions by different contributors have changed the project over time. 
- When working with multiple collaborators, understanding what commits are being incorporated into the repository and who commits were pushed are crucial to avoid breaking one another’s source code. 
- Collaborative environments developed around version control systems provide central repositories, issue tracking and threaded discussions which helps facilitate a team-based approach to the software development lifecycle.



# File Naming Convention (FNC)


- File naming convention is essentially a framework for naming files in a way that describes what they contain and how they relate to other files.
	- This helps to minimise the chances of files being misplaced or lost unintentionally due to poor organisation of files. Such a convention also enables users to locate files quickly

>[!File naming best practices:]
>- Files should be named consistently 
>- File names should be short but descriptive (<25 characters) (Briney, 2015) 
>- Avoid special characters or spaces in a file name 
>- Use capitals and underscores instead of periods or spaces or slashes 
>- Use date format ISO 8601: YYYYMMDD 
>- Include a version number (Creamer et al. 2014) 
>- Write down naming convention in data management plan



# Governance of personal data 

### Personal Data 

- Personal data refers to data about an individual who can be identified from that data, or from that data and other information to which the organisation has or is likely to have access. 
- Personal data can range from names and contact numbers to other types of data that form part of an individual’s record. 

- Personal data may include the following: 
	- Full name 
	- NRIC or passport number 
	- Photograph or video image of an individual 
	- Mobile telephone number 
	- Personal email address 
	- Thumbprint 
	- Name and residential address


# Personal Data Protection Act (PDPA)
### Definition:

- The Personal Data Protection Act (PDPA) is a data protection law comprising various rules that govern the collection, use, disclosure and care of personal data. 
- It recognises both the rights of individuals to protect their personal data, including rights of access and correction, as well as the needs of organisations to collect, use or disclose personal data for legitimate and reasonable purposes.

  

### Data Obligations

Organisations are required to abide by the following 9 main personal data obligations:

- Consent Obligation
	- Only collect, use or disclose personal data for purposes which an individual has given his or her consent.

- Purpose Limitation Obligation
	- An organisation may collect, use or disclose personal data about an individual for the purposes that a reasonable person would consider appropriate in the circumstances and for which the individual has given consent.

- Notification Obligation
	- Notify individuals of the purposes for which your organisation is intending to collect, use or disclose personal data on or before such collection, use or disclosure of personal data.

 
 - Access and Correction Obligation
	 - Upon request, the personal data of an individual and information about the ways in which his or her personal data has been or may have been used or disclosed within a year before the request should be provided. 
	 - However, organisations are prohibited from providing individuals access if the provision of the personal data or other information could reasonably be expected to cause harmful effects. Organisations are also required to correct any error or omission in an individual’s personal data that is raised by the individual.

- Accuracy Obligation
	- Make reasonable effort to ensure that personal data collected by or on behalf of your organisation is accurate and complete, if it is likely to be used to make a decision that affects the individual, or if it is likely to be disclosed to another organisation.

- Protection Obligation
	- Make reasonable security arrangements to protect the personal data that your organisation possesses or controls to prevent unauthorised access, collection, use, disclosure or similar risks.

- Retention Limitation Obligation
	- Cease retention of personal data or remove the means by which the personal data can be associated with particular individuals when it is no longer necessary for any business or legal purpose.


- Transfer Limitation Obligation
	- Transfer personal data to another country only according to the requirements prescribed under the regulations, to ensure that the standard of protection provided to the personal data so transferred will be comparable to the protection under the PDPA, unless exempted by the PDPC.

- Accountability Obligation
	- Make information about your data protection policies, practices, and complaints process available on request. Designate a Data Protection Officer to ensure that your organisation complies with the PDPA.



### The Do Not Call (DNC) Registry 

- lets you opt out of marketing messages addressed to your Singapore telephone number, such as those which promote or advertise a good or service, allowing you to have more control over the kind of messages you receive on your telephone, mobile phone or fax machine.


### National Registration Identification Card

Unique identifications for Citizens and PRs, containing sensitive information like address.

- Organizations are not allowed to collect, use, or disclose NRIC numbers unless required by law or necessary for identity verification.
- Partial NRIC or other identifiers like mobile numbers can be used for verification instead.