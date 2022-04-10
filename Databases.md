# Introduction to Databases

`Database` is a collection of related data and data is a collection of facts and figures that can be processed to produce information.

`database management system` stores data in such a way that it becomes easier to retrieve, manipulate, and produce information.

## Characteristics

* `Real-world entity` A modern DBMS is more realistic and uses real-world entities to design its architecture. It uses the behavior and attributes too.

    #### For example
    ```
     a school database may use students as an entity and their age as an attribute 
    ```

* `Relation-based tables` DBMS allows entities and relations among them to form tables. A user can understand the architecture of a database just by looking at the table names.

* `Isolation of data and application` A database system is entirely different than its data. A database is an active entity, whereas data is said to be passive, on which the database works and organizes. DBMS also stores metadata, which is data about data, to ease its own process.

* `Less redundancy` DBMS follows the rules of `normalization`, which splits a relation when any of its attributes is having redundancy in values. Normalization is a mathematically rich and scientific process that reduces data redundancy.

* `Consistency`  Consistency is a state where every relation in a database remains consistent. There exist methods and techniques, which can detect attempt of leaving database in inconsistent state. A DBMS can provide greater consistency as compared to earlier forms of data storing applications like file-processing systems.

* `Query Language`  DBMS is equipped with query language, which makes it more efficient to retrieve and manipulate data. A user can apply as many and as different filtering options as required to retrieve a set of data. Traditionally it was not possible where file-processing system was used.

* `ACID Properties`  DBMS follows the concepts of `Atomicity`, `Consistency`, `Isolation`, and `Durability` (normally shortened as ACID). These concepts are applied on transactions, which manipulate data in a database. ACID properties help the database stay healthy in multi-transactional environments and in case of failure.

* `Multiuser and Concurrent Access`  DBMS supports multi-user environment and allows them to access and manipulate data in parallel. Though there are restrictions on transactions when users attempt to handle the same data item, but users are always unaware of them.

* `Multiple views`  DBMS offers multiple views for different users. A user who is in the Sales department will have a different view of database than a person working in the Production department. This feature enables the users to have a concentrate view of the database according to their requirements.

* `Security` − Features like multiple views offer security to some extent where users are unable to access data of other users and departments. 

## Users
* `Administrators`  Administrators maintain the DBMS and are responsible for administrating the database. They are responsible to look after its usage and by whom it should be used. They create access profiles for users and apply limitations to maintain isolation and force security. Administrators also look after DBMS resources like system license, required tools, and other software and hardware related maintenance.

* `Designers`  Designers are the group of people who actually work on the designing part of the database. They keep a close watch on what data should be kept and in what format. They identify and design the whole set of entities, relations, constraints, and views.

* `End Users` End users are those who actually reap the benefits of having a DBMS. End users can range from simple viewers who pay attention to the logs or market rates to sophisticated users such as business analysts.


## Database Schema
A database schema defines how data is organized within a relational database; this is inclusive of logical constraints such as, table names, fields, data types, and the relationships between these entities

* `Logical Schema` It describes the database designed at logical level.
* `Physical Schema` It describes the database designed at physical level.
* `View Schema` It defines the design of the database at the view level.

## Database Keys

* `Primary Key` It is the first and foremost key which is used to uniquely identify a record.
* `Foreign key` a filed or item in a table that contains a value identifying rows in another table.
* `Composite Key` in the context of relational databases, is a combination of two or more columns in a table that can be used to uniquely identify each row in the table.

## Database Relationships

* One-To-One Relationship(1:1) :

This type of relationship allows only one record on each side of the relationship. The primary key relates to only one record (or none) in another table. For example, in a marriage, each spouse has only one other spouse. This kind of relationship can be implemented in a single table and therefore does not use a foreign key.

* One-To-Many Relationship(1:N) :

A one-to-many relationship allows a single record in one table to be related to multiple records in another table. Consider a business with a database that has Customers and Orders tables.

* Many-To-Many Relationship(N:N) :

This is a complex relationship in which many records in a table can link to many records in another table. For example, our business probably needs Customers and Orders tables, and likely also needs a Products table.





