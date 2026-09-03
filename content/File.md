---
tags:
  - file
  - theory
---
# Types of file

### Serial File

Serial files contain records which have no defined order. Specifically, they are stored in chronological order, that is, as each record is received it is stored in the next available storage position. This type of file organisation means that the records are in no particular order and therefore, to retrieve a single record, the whole file needs to be read from beginning to end. An example of a serial file would be a bank’s records of transactions.


### Sequential Files

Sequential files are serial files whose records are sorted in ascending or descending on a particular key field. Key fields contain values that are unique and sequential but not necessarily consecutive. They are the types of files suited to long term storage of data. Therefore, they can be considered as an alternative to a database but do note that primary keys in a database table are required to be unique but not to be sequential. In a sequential file, a particular record is found sequentially reading the value of the key field until the required value is found.




# File Path

### Absolute Path

Absolute file paths are the exact file location in the computer or server.

```
//website.com/assets/image.jpg
```

### Relative Path

Relative file path points to the location of the file in the root folder of an individual web
project with reference to the current working file. We usually use this in our coding and
programming projects.

```
../assets/image.jpg
```
