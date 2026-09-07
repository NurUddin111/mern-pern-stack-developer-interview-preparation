<h1 align="center">Database Interview Questions</h1>

## 🎯 Database Fundamentals

## Q01. What is a database and why is it necessary?

A database is a system used to store, organize, manage, and retrieve data for an application.

A database is necessary because applications need to store different types of data, such as users, products, orders, and payments. We also need to create, read, update, and delete this data when required.

A database keeps the data persistent, makes it easier to manage, and allows multiple users or applications to work with the data. That is why a database is an important part of most real-world applications.

## Q02. What is a DBMS?

DBMS stands for Database Management System. It is a software system that is used to store, manage, retrieve, and update data in a database.

It works between the application and the database. When an application wants to read, insert, update, or delete data, the DBMS handles these operations.

A DBMS also helps with data security, data consistency, and managing access for multiple users.

## Q03. What is the difference between DBMS and RDBMS?

DBMS is a software system that is used to store and manage data in a database. RDBMS is a type of DBMS that stores data using related tables.

In an RDBMS, we can create relationships between tables and use features such as primary keys, foreign keys, and constraints.

So, the main difference is that DBMS is a general concept, while RDBMS is a specific type of DBMS that follows the relational model.

## Q04. What are the different types of DBMS?

There are different types of DBMS based on how they organize and store data. The main types are Hierarchical DBMS, Network DBMS, Relational DBMS or RDBMS, Object-Oriented DBMS, and NoSQL DBMS.

An RDBMS stores data in tables and allows relationships between those tables. A NoSQL database can use different data models, such as documents, key-value pairs, wide-columns, or graphs.

For example, MySQL and PostgreSQL are RDBMS databases, while MongoDB is a document-based NoSQL database.

## Q05. What is a table in DBMS?

A table is a structure in a relational database that stores data in rows and columns.

A column represents a specific type of data, such as a name, email, or age. A row represents one complete record in the table.

A relational database can have multiple tables, and we can create relationships between those tables when needed.

## Q06. What is data redundancy in a database?

For example, if a user's name and email are stored again and again with every order, the same user information is being duplicated.

This can use extra storage and make updates more difficult. If we update the data in one place but forget another place, it can cause data inconsistency. In relational databases, normalization is commonly used to reduce unnecessary data redundancy.

## Q07. What is the difference between SQL and NoSQL databases?

The main difference between SQL and NoSQL databases is how they store and organize data.

SQL databases are usually relational databases. They store data in tables with rows and columns, and we can create relationships between different tables. They usually use a structured schema.

NoSQL databases do not use the traditional relational table model. They can store data as documents, key-value pairs, graphs, or wide columns, and they usually provide a more flexible data structure.

PostgreSQL and MySQL are examples of SQL databases, while MongoDB and Redis are examples of NoSQL databases.

The choice between SQL and NoSQL depends on the application's data structure, relationships, consistency requirements, and scaling needs.

## Q08. Why are NoSQL databases popular today?

NoSQL databases are popular because they can provide flexible data structures and can work well for applications that need to scale.

Many NoSQL databases do not require a strict relational schema, so it can be easier to handle data when its structure changes. They can also support horizontal scaling, which is useful for applications with large amounts of data and high traffic.

Because of these features, NoSQL databases can be a good choice for some modern, real-time, and large-scale applications. However, it does not mean that NoSQL is always better than SQL. The choice depends on the requirements of the application.

## Q09. What are the different types of NoSQL databases?

There are four main types of NoSQL databases: Document, Key-Value, Wide-Column, and Graph databases.

A Document database stores data as documents, such as MongoDB. A Key-Value database stores data as key-value pairs, such as Redis. A Wide-Column database uses a column-based structure and is useful for large-scale distributed data, such as Cassandra. A Graph database stores data as nodes and relationships, such as Neo4j.

The right type depends on the data structure and requirements of the application.

## 🎯 Data Modeling & Normalization

## Q10. What is normalization in databases?

Normalization is the process of organizing data in a relational database to reduce unnecessary data duplication and improve data consistency.

We usually normalize a database by dividing a large table into smaller related tables and creating relationships between them.

This reduces repeated data, makes updates easier, and helps prevent data inconsistency. Common normal forms include 1NF, 2NF, and 3NF.

## Q11. What are the different normal forms?

## Q12. What is denormalization?

## Q13. What is the difference between ACID and BASE properties?

## Q14. What are the ACID properties in DBMS?