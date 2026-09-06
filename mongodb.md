<h1 align="center">MongoDB Interview Questions</h1>

## 🎯 Fundamentals

## Q01. What is MongoDB and what are the its main features?

MongoDB is a NoSQL and document-oriented database. Instead of storing data in tables and rows like a relational database, MongoDB stores data in collections and documents. The documents are stored in BSON format, which is similar to JSON.

The main features of MongoDB are flexible schema, powerful querying, indexing, replication, and horizontal scaling through sharding. A flexible schema allows documents in the same collection to have different structures. Replication helps provide high availability, while sharding helps distribute large amounts of data across multiple servers.

## Q02. How does MongoDB differ from relational databases?

MongoDB and relational databases mainly differ in how they store and organize data. MongoDB is a NoSQL and document-oriented database, so it stores data in documents and collections. Relational databases like MySQL and PostgreSQL store data in tables and rows.

MongoDB usually uses a flexible schema, so documents in the same collection do not always need to have the same structure. Relational databases usually use a predefined schema. In MongoDB, related data can be embedded inside a document, while relational databases usually store related data in separate tables and use foreign keys to create relationships.

MongoDB also provides good support for horizontal scaling and sharding. However, the choice between MongoDB and a relational database depends on the requirements of the application.

## Q03. Can you describe the structure of data in MongoDB?

MongoDB organizes data in a hierarchical structure. A database contains collections, and collections contain documents. Each document contains different fields.

We can roughly compare a MongoDB collection with a table and a document with a row in a relational database. Each document has a unique \_id field. A field can also contain arrays or nested documents, which allows MongoDB to store complex data structures.

## Q04. What is Document in MongoDB?

A document is the basic unit used to store data in MongoDB. It stores data as key-value pairs and looks similar to a JSON object. A document can contain different fields, arrays, and nested documents. Each document has a unique \_id field. MongoDB stores documents in BSON format.

## Q05. How is data stored in collection in MongoDB?

In MongoDB, data is stored as documents inside a collection. Each document contains data in the form of key-value pairs and can contain different fields, arrays, or nested documents. A collection can contain many documents, and the documents do not always need to have the same structure because MongoDB has a flexible schema. MongoDB stores these documents internally in BSON format.

## Q06. Describe what a MongoDB database is.

A MongoDB database is a container that holds one or more related collections. Each collection contains documents, and each document contains fields. So, the basic structure of MongoDB is Database, Collection, Document, and Field. For example, an e-commerce database can contain collections such as users, products, and orders.

## Q07. What is the default port on which MongoDB listens?

The default port for MongoDB is 27017. When MongoDB runs with its default configuration, it listens for client connections on this port. For a local MongoDB server, we commonly use localhost:27017.

## Q08. How does MongoDB provide high availability and disaster recovery?

MongoDB provides high availability mainly through replica sets. A replica set contains a primary server and one or more secondary servers. The primary usually handles write operations, and the secondary servers replicate the data from the primary.

If the primary server fails, one of the secondary servers can be elected as the new primary. This helps the application continue working with minimal interruption. For disaster recovery, regular backups are also important because backups allow us to restore data after serious failures or accidental data loss.

## Q09. What are the indexes in MongoDB, and why are they used?

An index in MongoDB is a special data structure that helps MongoDB find documents faster. If we frequently search or filter data using a particular field, we can create an index on that field. This can prevent MongoDB from scanning every document in the collection and can make queries much faster.

However, indexes also have a cost. They require extra storage and MongoDB needs to maintain them when we insert, update, or delete documents. So, we should create indexes only on fields that need them. MongoDB automatically creates a unique index on the \_id field of every collection.

## Q10. what is the role of the id field in MongoDB documents?

The \_id field is a unique identifier for a document in MongoDB. It is used to uniquely identify each document inside a collection. If we do not provide an \_id when inserting a document, MongoDB automatically creates an ObjectId for it. MongoDB also automatically creates a unique index on the \_id field.

# 🎯 CRUD Operations

## Q11. How do you create a new MongoDB collection?

We can create a MongoDB collection using the db.createCollection() method. For example, db.createCollection("users") creates a collection called users. However, we do not always need to create a collection manually. If we insert a document into a collection that does not exist, MongoDB can automatically create the collection and insert the document.

## Q12. What is the syntax to insert a document into a MongoDB collection?

We use the insertOne() method to insert a single document into a MongoDB collection. The syntax is db.collectionName.insertOne({ ... }), where we provide the collection name and the document that we want to insert. If we want to insert multiple documents, we can use the insertMany() method.

## Q13. Describe how to read data from a MongoDB collection.

## Q14. Explain how to update Documents in MongoDB.

## Q15. What are the MongoDB commands for deleting documents?

## Q16. Can you join two collections in MongoDB? If so, how?

## Q17. How do you limit the number of documents returned by a MongoDB query?

## Q18. What is the difference between find() and findOne() in MongoDB?

## Q19. How can you achieve pagination in MongoDB?

## Q20. What are the differences between MongoDB’s insertOne and insertMany methods?
