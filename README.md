# Redis
NoSQL is a database technology that stores data in flexible schemas that scale easily. For decades, the predominant data model in application development was the relational data model that stored data in tables made of rows and columns. Structured Query Language (SQL) was used to create and edit these relational tables. It wasn’t until the mid to late 2000s that other flexible data models began to gain significant adoption and usage. To differentiate and categorize these new classes of databases and data models, the term NoSQL was coined. NoSQL stands for not only SQL or non-SQL. Often the term NoSQL is used interchangeably with the term non-relational.

## What are the advantages of NoSQL databases
Modern applications face several challenges that can be solved by NoSQL databases. For instance, applications process a large data volume from disparate sources like social media, smart sensors, and third-party databases. All of this disparate data doesn't fit neatly into the relational model. Enforcing tabular structures can lead to redundancy, data duplication, and performance issues at scale.

NoSQL databases are purpose-built for non-relational data models and have flexible schemas for building modern applications. They are widely recognized for their ease of development, functionality, and performance at scale. Benefits of NoSQL databases are listed below.

### 1. Flexibility
NoSQL databases generally provide flexible schemas that enable faster and more iterative development. The flexible data model makes NoSQL databases ideal for semi-structured and unstructured data.

### 2. Scalability
NoSQL databases are typically designed to scale out by using distributed clusters of hardware, as opposed to scaling up by adding expensive and robust servers. Some cloud providers handle these operations behind the scenes as a fully managed service.

### 3. High performance
NoSQL databases are optimized for specific data models and access patterns. These enable higher performance than if you were trying to accomplish similar functionality with relational databases.

### 4. Highly functional
NoSQL databases provide highly functional APIs and data types that are purpose-built for each of their respective data models.

## What are the use cases of NoSQL databases
You can use NoSQL databases to build a wide variety of high-performance mobile, Internet of Things (IoT), gaming, and web applications that provide great user experiences at scale. The range of NoSQL databases and their respective uses cases are wide-ranging. While it is challenging to present a representative set of use cases, below we provide a few illustrative examples as thought-starters and encourage you to learn more about each NoSQL database and their respective uses cases.

### 1. Real-time data management
You can deliver real-time recommendations, personalization, and improved user experiences with NoSQL databases. For example, Disney+ delivers its extensive digital content library to over 150 million+ subscribers using NoSQL database technology. It can scale and deliver popular features such as Continue Watching, Watchlist, and Personalized Recommendations with Amazon DynamoDB.

### 2. Cloud security
You can use graph databases to quickly discover complex relationships within your data. For instance, Wiz re-imagined cloud security as a graph using Amazon Neptune. Wiz helps their customers improve their security posture by quickly identifying and fixing the most critical risks. They use graph model stored in Amazon Neptune to uncover the toxic combination of risk factors that represent critical risks. The Wiz risk engines traverse the graph and within seconds, weave together a series of interconnected risks factors in a security graph.

### 3. High-availability applications
Distributed NoSQL databases are excellent for building high-availability, low-latency applications for messaging, social media, file sharing, and more. For example, Snapchat has more than 290 million users sending billions of pictures and video messages daily. It uses NoSQL database systems to reduce the median latency of sending messages by 20%.

## How do NoSQL databases work
NoSQL databases use a variety of data models for accessing and managing data. There are differences in implementation based on the data model. However, many NoSQL databases use Javascript Object Notation (JSON), an open data interchange format that represents data as a collection of name-value pairs.

### 1. NoSQL database example
Consider this example of modeling the schema for a simple book database:

+ In a relational database, a book record is often disassembled (or “normalized”) and stored in separate tables, and relationships are defined by primary and foreign key constraints. In this example, the Books table has columns for ISBN, Book Title, and Edition Number; the Authors table has columns for AuthorID and Author Name; and finally, the Author-ISBN table has columns for AuthorID and ISBN. The relational model is designed to enable the database to enforce referential integrity between tables in the database, normalized to reduce the redundancy, and generally optimized for storage.
+ In a NoSQL database, a book record is usually stored as a document. For each book, the item, ISBN, Book Title, Edition Number, Author Name, and AuthorID are stored as attributes in a single document. In this model, data is optimized for intuitive development and horizontal scalability.
### NoSQL terminology
The following table compares terminology used by select NoSQL databases with terminology used by SQL databases.
|SQL	|MongoDB	|DynamoDB	|Cassandra 	|Couchbase|
|:--- |:--- |:--- |:--- |:--- |
|Table	|Collection	|Table	|Table |Data bucket|
|Row	|Document	|Item	|Row	|Document|
|Column	|Field	|Attribute	|Column	|Field|
|Primary key	|ObjectId	|Primary key |Primary key	|Document ID|
|Index	|Index	|Secondary index	|Index	|Index|
|View	|View	|Global secondary index	|Materialized view	|View|
|Nested table or object	|Embedded document	|Map	|Map	|Map|
|Array	|Array	|List	|List	|List| 
 
## What are the types of NoSQL databases
There are several different NoSQL database systems due to variations in the way they manage and store schema-less data. We explain some of the common types below.

### 1. Key-value databases
Key-value databases are highly partitionable and allow horizontal scaling at a level that other types of NoSQL databases may not achieve. A key-value database stores data as a collection of key-value pairs in which a key serves as a unique identifier. Keys and values can be anything, ranging from simple objects to complex compound objects. Use cases such as gaming, ad tech, and IoT lend themselves particularly well to the key-value store data design.

### 2. Document databases
Document-oriented databases have the same document model format that developers use in their application code. They store data as JSON objects that are flexible, semi-structured, and hierarchical in nature. The document database model works well with catalogs, user profiles, and content management systems, where each document is unique and evolves over time.

### 3. Graph databases
Graph databases are purpose-built to store and navigate relationships. They use nodes to store data entities and edges to store relationships between entities. An edge always has a start node, end node, type, and direction. It can describe parent-child relationships, actions, ownership, and the like. There is no limit to the number and kind of relationships a node can have. You can use a graph database to build and run applications that work with highly connected datasets. Typical use cases for a graph database include social networking, recommendation engines, fraud detection, and knowledge graphs.

### 4. In-memory databases
While other non-relational databases store data on disk or SSDs, in-memory data stores are designed to eliminate the need to access disks. They are ideal for applications that require microsecond response times or have large spikes in traffic. You can use them in gaming and ad-tech applications for features like leaderboards, session stores, and real-time analytics.

### 5. Search databases
A search-engine database is a type of non-relational database that is dedicated to the search of data content. It uses indexes to categorize similar characteristics among data and facilitate search capability. Search-engine databases are optimized for sorting unstructured data like images and videos. They can provide near-real-time visualizations and analytics by indexing, aggregating, and searching semi-structured data like logs and metrics.

## What are the differences between NoSQL and SQL databases
SQL databases model data relationships as tables. The rows in the table represent a collection of related values of one object or entity. Each column in the table represents a data attribute, and a field (or table cell) stores the actual value of the attribute. You can use a relational database management system (RDBMS) to access the data in many different ways without reorganizing the database tables themselves. Key differences between relational and non-relational databases are given in the table below.

 

| |Relational databases |NoSQL databases|
|:--- |:--- |:--- |
Optimal workloads|Relational databases are designed for transactional and strongly consistent online transaction processing (OLTP) applications. They are also good for online analytical processing (OLAP).|NoSQL databases are designed for a number of data access patterns that include low-latency applications. NoSQL search databases are designed for analytics over semi-structured data.|
|Data model|The relational model normalizes data into tables that are composed of rows and columns. A schema strictly defines the tables, rows, columns, indexes, relationships between tables, and other database elements. The database enforces referential integrity in relationships between tables.

NoSQL databases provide a variety of data models, such as key-value, document, graph, and column, which are optimized for performance and scale.

ACID properties

Relational databases provide atomicity, consistency, isolation, and durability (ACID) properties:

Atomicity requires a transaction to execute completely or not at all.
Consistency requires that the data must conform to the database schema when a transaction has been committed.
Isolation requires that concurrent transactions execute separately from each other.
Durability requires the ability to recover from an unexpected system failure or power outage to the last known state.
Most NoSQL databases offer trade-offs by relaxing some of the ACID properties of relational databases in favor of a more flexible data model that can scale horizontally. This makes NoSQL databases an excellent choice for high-throughput, low-latency use cases that need to scale horizontally beyond the limitations of a single instance.

Performance

Performance is generally dependent on the disk subsystem. The optimization of queries, indexes, and table structure is often required to achieve peak performance.

Performance is generally a function of the underlying hardware cluster size, network latency, and the calling application.

Scale

Relational databases typically scale up by increasing the compute capabilities of hardware or scale out by adding replicas for read-only workloads.

NoSQL databases are typically partitionable. This is because access patterns can scale out by using distributed architecture to increase throughput that provides consistent performance at near-boundless scale.

APIs

Requests to store and retrieve data are communicated using queries that conform to a structured query language (SQL). These queries are parsed and executed by the relational database.

Object-based APIs allow app developers to easily store and retrieve data structures. Partition keys let apps look up key-value pairs, column sets, or semi-structured documents that contain serialized app objects and attributes.

 
When should you choose NoSQL databases over SQL databases
A NoSQL database is best for handling indeterminate, unrelated, or rapidly changing data. It is intuitive to use for developers when the application dictates the database schema. You can use it for applications that:

Prioritize performance over strong data consistency and maintaining relationships between data tables (referential integrity).
Require horizontal scaling by sharding across servers.
You don't always have to choose between a non-relational and relational database schema. You can employ a combination of SQL and NoSQL databases in your applications. This hybrid approach is quite common and ensures each workload is mapped to the right database for optimal price performance.

