---
tags:
  - database
  - practical
---
## Terms used in NoSql

|**MongoDB Term**|**SQL Term**|
|---|---|
|Database|Database|
|Collection|Table|
|Document|Row/Record|
|Field|Field/Column|

|**Operator**|**Description**|
|---|---|
|`$eq`|Equal to|
|`$ne`|Not equal to|
|`$gt`|Greater than|
|`$gte`|Greater than or equal to|
|`$lt`|Less than|
|`$lte`|Less than or equal to|
|`$in`|Matches any value specified in an array|
|`$nin`|Matches if the value is not equal to any of a given list of values.|
|`$or`|Logical or|
|`$and`|Logical and|
|`$not`|Logical not|
|`$exists`|Matches documents which has the named field|
|`$set`|Sets the a specified field to a given value|
|`$unset`|Removes a specified field from specified documents|

## CRUD

- C → Create
    
- R → Read
    
- U → Update
    
- D → Delete
    

## ACID

When discussing databases, the most common question you will hear is asking whether it is ACID compliant. ACID stands for **A**tomicity, **C**onsistency, **I**solation, and **D**urability.

### Atomicity

Atomicity is all based around this idea of togetherness. When carrying out any kind of database constraints, it often consists of multiple operations. With atomicity, **either every operation succeeds or none of them do**. This is important because the operations can have an impact on each other, so one failing can lead to unexpected results.

Think of a financial transaction, for example. You are paying a friend $250 for a holiday you are going on. The whole transaction would consist of the money leaving your account and arriving in the recipient’s account. If there was no atomicity, it is possible that money leaves your account but doesn’t arrive at the other end, resulting in you being debited the money but still owning the recipient.

### Consistency

Consistency is about ensuring that changes made as part of a transaction are **consistent with any database constraints**. If the data at any stage goes against these constraints, the whole transaction will fail.

Unless you have an agreed overdraft, banks, for example, will expect your balance to be positive. So if you tried to withdraw more money than you have available, this would break a constraint and fail, rolling back all operations in the transaction.

### Isolation

Isolation is there to **make sure that all transactions are run in an isolated environment** **without interfering with each other**.

Sticking with the financial example, imagine you have a bank balance of $200 and you try to withdraw $100 at an ATM. At the same time, a standing order you have set up comes out for $100. With isolation, these transactions can occur concurrently, ensuring that your ending balance is $0, not $100, because the transaction impacted each other.

### Durability

Durability is another important element of ACID because it ensures that no matter what happens, once a transaction is complete, the **changes in that transaction are written into the database**. This makes sure that **data changes are persisted**, even in the event of a power failure or system crash.


# Advantages of NoSQL

| Feature                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Flexibility**        | Having a flexible data model also means NoSQL databases can address large volumes of rapidly changing data, making them great for agile development, quick iterations, and frequent code pushes.                                                                                                                                                                                                                                                   |
| **Cost-effectiveness** | NoSQL databases are typically designed to scale out horizontally by using distributed clusters of hardware, as opposed to scaling up by adding expensive and robust servers.                                                                                                                                                                                                                                                                       |
| **Fast queries**       | Queries in NoSQL databases can be faster than SQL databases. Data in SQL databases is typically normalized, so queries for a single object or entity require you to join data from multiple tables. As the tables grow in size, the joins can become expensive. However, data in NoSQL databases is typically stored in a way that is optimized for queries. Queries typically do not require joins, so the queries are simpler and are very fast. |
| **Replication**        | NoSQL replication functionality copies and stores data across multiple servers. This replication provides data reliability, ensuring access during downtime and protecting against data loss if servers go offline.                                                                                                                                                                                                                                |

# Difference between NoSQL and SQL

| Feature              | Relational databases                                                                                                          | NoSQL databases                                                                                                                                                                      |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Language**         | Use structured query languages to perform operations                                                                          | Use a dynamic schema to query data. Also, some NoSQL databases use SQL-like syntax for document manipulation.                                                                        |
| **Data Schema**      | Have a predefined and fixed format, which cannot be changed for new data.                                                     | NoSQL databases are more flexible. This flexibility means that records in the databases can be created without having a predefined structure, and each record has its own structure. |
| **Scalability**      | Is vertically scalable, meaning that a single machine needs to increase CPU, RAM, SSD, at a certain level to meet the demand. | horizontally scalable, meaning that additional machines are added to the existing infrastructure to satisfy the storage demand.                                                      |
| **Big Data Support** | The vertical scaling makes it difficult for relational databases to store very big data                                       | The horizontal scaling and dynamic data schema make NoSQL suitable for big data.                                                                                                     |
| **Properties**       | Use the ACID (Atomicity, Consistency, Isolation, Durability) property.                                                        | Settles for eventual consistency                                                                                                                                                     |

# Application of NoSQL databases

### Social Media: 

Social media platforms handle large volumes of unstructured data, such as user profiles, posts, and interactions. The flexibility of NoSQL accommodates the dynamic nature of social media content and data. 

### Logistics and Supply Chain:

They use NoSQL databases for real-time tracking of shipments, inventory management, and other diverse and dynamic data sources across the supply chain. NoSQL’s performance and scalability for real-time data make it well suited for this industry. 

### Gaming:

The gaming industry leverages NoSQL databases for managing player data, leaderboards, and in-game analytics. The ability to scale horizontally is essential for handling the massive amounts of data generated by online multiplayer games.



# Application of SQL databases

### Finance: 

Many financial institutions manage transactional data and customer records. SQL’s ACID properties ensure the data are accurate and that the transactions lead to an immediately consistent database once processed. 

### Retail:

Many retail businesses leverage SQL databases, as they must manage complex relationships related to products, shipping, sales, customers, and supplier information. Their data are also typically well-structured and predictable. 

### Government and Public Sector: 

Government agencies manage a lot of citizen records and public services which are subject to regulatory requirements. SQL’s structured nature helps with regulatory adherence.

# Syntax

### Importing mongodb into python:

```python
import pymongo
```

### Printing out databases:

```python
import pymongo
client = pymongo.MongoClient("127.0.0.1", 27017)
databases = client.database_names()
print("The databases in the MongoDB server are:")
print(databases)
client.close()
```

### Inserting data:

```python
import pymongo
client = pymongo.MongoClient("127.0.0.1", 27017)
db = client.get_database("entertainment")
coll = db.get_collection("movies")

# Using .insert_one(<dict>)

coll.insert_one({"_id":1, "title":"Johnny Maths", "genre":"comedy"})
coll.insert_one({"title":"Star Walls", "genre":"science fiction"})
coll.insert_one({"title":"Detection"}) # no genre

# Using .insert_many(<list of dicts>)

list_to_add = []
list_to_add.append({"title":"Badman", "genre":"adventure", "year":2015})
list_to_add.append({"title":"Averages", "genre":["science fiction", "adventure"], "year":2017})
list_to_add.append({"title":"Octopus Man", "genre":"adventure", "year":2017})
list_to_add.append({"title":"Fantastic Bees", "genre":"adventure", "year":2018})
list_to_add.append({"title":"Underground", "genre":"horror", "year":2014})
coll.insert_many(list_to_add)

c = db.collection_names("entertainment")
print("Collections in entertainment database: ", c)
client.close()
```

Note: For line 3, MongoDB waits until you have inserted at least one document before it actually creates the database and collection.

### Reading JSON (JavaScript Object Notation) file

```python
import pymongo, json
client = pymongo.MongoClient("127.0.0.1", 27017)
with open("input.json") as file:
    data = json.load(file)
client['entertainment']['moreusers'].insert_many(data)
client.close()
```

### Querying Documents

```python
import pymongo

client = pymongo.MongoClient('127.0.0.1', 27017)
db = client.get_database("entertainment")
coll = db.get_collection("movies")

# Querying for all documents in movies

result = coll.find()
print("All documents in movie collection: ")
for document in result:
    print(document)
print("Number of items in movie collection:", coll.count())

# Querying for all documents in movies with adventure genre

result = coll.find({'genre': 'adventure'})
print("All movies with adventure genre: ")
for document in result:
    print(document)

# Querying for all documents in movies with adventure genre that is made after 2016

query2 = {'genre': 'adventure', 'year':{'$gt':2016}}
result = coll.find(query2)
print("All titles of movies with adventure genre after 2016:")
for document in result:
    print(" - " + document.get('title'))
print("There are", result.count(), "movies in the list above.")

client.close()
```

### More queries

```python
import pymongo

client = pymongo.MongoClient('127.0.0.1', 27017)
db = client.get_database("entertainment")
coll db.get_collection("movies)

result = coll.find()
print("All documents in movie collection:")
for document in result:
    print(document)
print("Number of items in movie collection:", coll.count())

result = coll.find({'genre':{'$in':['adventure', 'comedy'}})
print("All movies with adventure or comedy genre inside:")
for document in result:
    print(document)

query2 = {'genre':{'$exists':False}}
result = coll.find(query2)
print("All movies without genre:")
for document in result:
    print(" - " + document.get('title'))

result = coll.find_one({'year':{'$eq':2017}})
print("One movie that was released in 2017")
print(result)
client.close()
```

### Updates:

```python
import pymongo

client = pymongo.MongoClient('127.0.0.1', 27017)
db = client.get_database('entertainment')
coll = db.get_collection('movies')

result = coll.find()
print("All documents in movies collection:")
for document in result:
    print(document)

search = {'year':{'$gt':2016}}
update = {'$set':{'year':2015}}
coll.update_one(search, update)

result = coll.find()
print("All documents in movies collection after update one:")
for document in result:
    print(document)

coll.update_many(search, update)

result = coll.find()
print("All documents in movies collection after update many:")
for document in result:
    print(document)

search = {'year':{'$eq':2018}}
update = {'$unset':{'year':0}}
coll.update_many(search, update)

result = coll.find()
print("All documents in movies collection after unset:")
for document in result:
    print(document)

client.close()
```

For line 28, the second parameter for `$unset` is ignored (you can put anything). All it does is that it removes the given field indicated in the first parameter.

### Deleting documents:

```python
import pymongo

client = pymongo.MongoClient('127.0.0.1', 27017)
db = client.get_database('entertainment')
coll = db.get_collection('movies')

result = coll.find()
print("All documents in movies collection:")
for document in result:
    print(document)

coll.delete_one({'year':2015})

result = coll.find()
print("All documents in movies collection after deleting one:")
for document in result:
    print(document)

coll.delete_many({'year':2015})

result = coll.find()
print("All documents in movies collection after deleting all:")
for document in result:
    print(document)

client.close()
```

### Dropping collections:

```python
import pymongo

client = pymongo.MongoClient('127.0.0.7', 27017)
db = client.get_database('entertainment')
coll = db.get_collection('tv')

coll.insert_one({"title":"X Man", "genre":"science fiction"})
coll.insert_one({"title":"Fresh from the boat", "genre":"comedy"})
coll.insert_one({"title":"", "genre":"comedy"})
coll.insert_one({"genre":"comedy"})

result = coll.find()
print("All documents in tv collection:")
for document in result:
    print(document)
print("Number of items in tv collection:", coll.count())

db.drop_collection('tv')

result = coll.find()
print("After tv collection is dropped:")
for document in result:
    print(document)
print("Number of items in tv collection:", coll.count())

client.close()
```

### Removing databases:

```python
client.drop_database("entertainment")
```