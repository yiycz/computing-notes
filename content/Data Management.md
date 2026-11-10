
---
tags:
  - theory
  - data-management
---
# Data lifestyle

The data life cycle refers to the **entire period of time that data exists in the system**. This life cycle encompasses **all the stages that the data goes through**, from its **creation to its eventual disposal**, encompassing the entire lifespan of data within an organisation or system.

```mermaid
flowchart LR
    A[Creation] --> B[Storage]
    B --> C[Usage]
    C --> D[Archival]
    D --> E[Destruction]
```

# Data Integrity

Data integrity refers to the **accuracy and validity of data**.


|Cause|Elaboration|
|---|---|
|Hardware failure|Secondary devices may experience **wear and tear** over time, **reducing reliability** and **increasing the risk of data loss**|
|Human Actions|Humans may **accidentally delete or overwrite data**. They may also **format or partition the wrong drive** or **handle storage media improperly**, leading to **data loss**|
|Power Failures|**Sudden power outages or voltage fluctuations** can **interrupt data transfers or damage storage devices**, leading to **data loss**|
|Malware and ransomware|Malicious software can **encrypt, delete, or compromise data**, making it **inaccessible unless a ransom is paid**.|


## Backup

Backing up means **making a copy of the data** and **storing it on a different storage device**. 

It is to create a **recoverable copy** of the data if the original data is **corrupted**. 

## Archive

Data archival refers to the process of **identifying, organising and storing data** in a **secure and accountable manner**.

It is for compliance and legal purpose 

|Key considerations|Elaboration|
|---|---|
|Data Classification|Data should be **prioritised based on its value, sensitivity, and legal/regulatory requirements** to determine the **appropriate archival strategy**.|
|Retention Policies|The **period of retention** for the archived data must be based upon **legal, industry or organisational requirement**, taking into consideration factors like **sensitivity and business needs**|
|Storage infrastructure|To ensure **cost-efficiency**, it is important to adopt a **scalable and reliable storage system** capable of **accommodating large volumes of data over extended periods**|
|Metadata and indexing|**Descriptive metadata and indexing mechanisms** can be implemented to facilitate **efficient search and retrieval of archived data**.|
|Data security|Archived data should be **protected against unauthorized access, tampering, and data breaches** by implementing **appropriate security controls**.|
|Data integrity and preservation|**Data integrity checks, periodic validation, and migration strategies** should present the **integrity and usability of archived data over time**.|

|Importance of data archival|Elaboration|
|---|---|
|Regulatory Compliance|Archiving data helps organizations **meet legal and regulatory requirements**, such as **data retention periods** mandated by industry-specific regulations.|
|Litigation and e-Discovery|Archived data can be **crucial in legal proceedings**, enabling organizations to **retrieve and present evidence** when required.|
|Historical Analysis|Archiving data allows for **retrospective analysis and trend identification**, aiding in **strategic decision-making and historical research**.|
|Disaster Recovery|While the archived copy of the data may not be the latest backup copy of the data, it can still **serve as a backup** in the event of **data loss or system failures**, ensuring **business continuity**.|

## Archive vs backup

|                       | Backup                                                                                | Archive                                                                          |
| --------------------- | ------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| Data Storage Method   | The **original data remains in place**, while a **backup copy is stored in another location** | **Archived data is moved from its original location** to an **archive storage location** |
| Data State            | Backed-up data is **constantly changing**                                                 | Once you create an archive, you **do not modify it**                                 |
| Data Retention Policy | You **periodically delete or overwrite data backups** that are too old to be useful       | Data archives are designed for **long-term storage**                                 |
| Storage Type          | **Hot cloud storage or easily accessible local storage locations**                        | **Cold cloud storage or tape archives**                                              |
| Data Scope            | **All of your data**, with the exception of unimportant information like temporary files  | **Specific files** that you must retain for **compliance purposes**                      |

## Version Control

Version control is defined as a system that **tracks the progress of code across the software development lifecycle and its multiplier iterations** - which **maintains a record of every change** complete with **authorship, timestamp, and other details** - and also aids in **managing change**.

### Significance

- **Easy modification of the codebase**: Version control allows developers to **maintain source code, documentation and configuration files**, storing different versions **safely and systematically**. This makes it easier to **manage modifications, updates and new features** throughout software development.

- **Track changes**: Version control maintains a **history of changes** made to documents, including **who made changes and when** they were done. This allows the team to easily **revert to previous versions** if needed.

- **Enables collaboration**: Version control ensures that **multiple team members can work on the same documentation simultaneously** without **overwriting each other’s contributions**. It provides a structured way to **manage revisions and resolve conflicts** among contributors.

# File Naming Convention (FNC)

- File naming convention is essentially a **framework for naming files** in a way that **describes what they contain** and **how they relate to other files**.

Naming conventions are needed to **ensure consistency and clarity** in how files are named. They make it **easier to identify specific documents (and their versions) quickly**, and to **understand the content / purpose of the file without opening it**. An example of a file with good naming convention would be “UserGuide_v1.3_2025-11-10.md”.

>[!File naming best practices:]
>- Files should be **named consistently**
>- File names should be **short but descriptive** (<25 characters) (Briney, 2015)
>- **Avoid special characters or spaces** in a file name
>- Use **capitals and underscores** instead of periods or spaces or slashes
>- Use **date format ISO 8601: YYYYMMDD**
>- **Include a version number** (Creamer et al. 2014)
>- **Write down naming convention in data management plan**

# Governance of personal data

# Personal Data Protection Act (PDPA)

### Definition:

**Personal data** refers to **data about an individual who can be identified from that data**, or from that data and **other information to which the organisation has or is likely to have access**.

- The Personal Data Protection Act (PDPA) is a **data protection law** comprising various rules that **govern the collection, use, disclosure and care of personal data**.
- It recognises both the **rights of individuals to protect their personal data**, including **rights of access and correction**, as well as the **needs of organisations to collect, use or disclose personal data** for **legitimate and reasonable purposes**.

### Data Obligations

Organisations are required to abide by the following **9 main personal data obligations**:

- **Consent Obligation**
    - Only **collect, use or disclose personal data** for purposes which an individual has **given his or her consent**.

- **Purpose Limitation Obligation**
    - An organisation may **collect, use or disclose personal data** about an individual for the **purposes that a reasonable person would consider appropriate in the circumstances** and for which the individual has **given consent**.

- **Notification Obligation**
    - **Notify individuals of the purposes** for which your organisation is intending to **collect, use or disclose personal data** **on or before such collection, use or disclosure** of personal data.

- **Access and Correction Obligation**
    - Upon request, the **personal data of an individual** and **information about the ways in which his or her personal data has been or may have been used or disclosed within a year before the request** should be **provided**.
    - However, organisations are **prohibited from providing individuals access** if the provision of the personal data or other information could reasonably be expected to **cause harmful effects**. Organisations are also required to **correct any error or omission** in an individual’s personal data that is raised by the individual.

- **Accuracy Obligation**
    - Make **reasonable effort** to ensure that personal data collected by or on behalf of your organisation is **accurate and complete**, if it is likely to be **used to make a decision that affects the individual**, or if it is likely to be **disclosed to another organisation**.

- **Protection Obligation**
    - Make **reasonable security arrangements** to **protect the personal data** that your organisation possesses or controls to **prevent unauthorised access, collection, use, disclosure or similar risks**.

- **Retention Limitation Obligation**
    - **Cease retention of personal data** or **remove the means by which the personal data can be associated with particular individuals** when it is **no longer necessary for any business or legal purpose**.

- **Transfer Limitation Obligation**
    - **Transfer personal data to another country** only according to the **requirements prescribed under the regulations**, to ensure that the **standard of protection** provided to the personal data so transferred will be **comparable to the protection under the PDPA**, unless exempted by the PDPC.

- **Accountability Obligation**
    - **Make information about your data protection policies, practices, and complaints process available on request**. **Designate a Data Protection Officer** to ensure that your organisation **complies with the PDPA**.

### The Do Not Call (DNC) Registry

- lets you **opt out of marketing messages** addressed to your **Singapore telephone number**, such as those which promote or advertise a good or service, allowing you to have **more control over the kind of messages you receive** on your telephone, mobile phone or fax machine.

### National Registration Identification Card

**Unique identifications for Citizens and PRs**, containing **sensitive information like address**.

- Organizations are **not allowed to collect, use, or disclose NRIC numbers** unless **required by law or necessary for identity verification**.
- **Partial NRIC or other identifiers like mobile numbers** can be used for **verification instead**.
