# Database Fundamentals

## Introduction to Databases

- **What is a database?**
  A database is a structured collection of data organized in a way that allows for efficient storage, retrieval, and manipulation of information. It acts as a centralized repository for storing and managing data, providing a systematic and organized approach to data management.

  Databases are designed to store data in a structured and organized manner, using tables, rows, and columns. Each row in a table represents a unique entry or record, and columns represent the different attributes or fields associated with that entry. This structured approach ensures data integrity, consistency, and accessibility.

- **Purpose and importance of databases**
  Databases serve several crucial purposes in various domains, including:

  1. **Data organization and management**: Databases provide a systematic way to store, organize, and manage large amounts of data, making it easier to access, update, and retrieve information as needed.

  2. **Data integrity and consistency**: Databases enforce rules and constraints to ensure data integrity and consistency, preventing issues like duplicate entries, missing or incorrect data, and inconsistent relationships between data elements.

  3. **Data security and access control**: Databases offer mechanisms for controlling access to data, ensuring that only authorized users or applications can view, modify, or delete sensitive information.

  4. **Data sharing and collaboration**: Databases enable multiple users or applications to access and work with the same data concurrently, facilitating data sharing and collaboration within an organization or across different systems.

  5. **Data analysis and reporting**: Databases provide powerful querying and reporting tools, allowing users to extract meaningful insights, generate reports, and make informed decisions based on the stored data.

  6. **Application integration**: Databases serve as the backbone for many applications, enabling them to store, retrieve, and manipulate data efficiently, facilitating seamless integration and interoperability across different software systems.

- **Types of databases**
  There are several types of databases, each designed to meet specific data storage and retrieval requirements:

  1. **Relational databases**: These databases store data in tables with predefined relationships between them. Examples include MySQL, PostgreSQL, Oracle, and SQL Server. Relational databases use Structured Query Language (SQL) for data manipulation and querying.

  2. **NoSQL databases**: NoSQL (Not only SQL) databases are non-relational databases that store and manage data in a flexible and schema-less manner. They are designed to handle large volumes of unstructured or semi-structured data. Examples include MongoDB (document-oriented), Cassandra (wide-column store), Redis (key-value store), and Neo4j (graph database).

  3. **In-memory databases**: These databases store data entirely in-memory, providing extremely fast read and write operations. Examples include Redis and Memcached, often used as caching systems or for real-time data processing.

  4. **Cloud databases**: With the rise of cloud computing, many database solutions are now offered as cloud-based services, such as Amazon RDS, Google Cloud SQL, and Azure SQL Database. These services provide managed database instances, scalability, and seamless integration with other cloud services.

  5. **Object-oriented databases**: These databases store data as objects, similar to the way object-oriented programming languages represent data. They are particularly useful for applications that require complex data structures and relationships.

  6. **Time-series databases**: Designed for storing and processing time-stamped data, time-series databases are optimized for handling large volumes of time-series data, such as sensor readings, financial data, or application metrics.

The choice of database type depends on factors such as the nature of the data, performance requirements, scalability needs, and the specific use case or application domain.

## Data Models

- **Hierarchical data model**
  The hierarchical data model organizes data in a tree-like structure, with a single root node representing the top-level entity, and child nodes representing subordinate entities. This model is based on the parent-child relationship, where each child node can have only one parent node, but a parent node can have multiple child nodes.

  In the hierarchical model, data is organized into a series of records, and each record can have one or more fields. The records are linked together through links or pointers, forming a hierarchical structure. Data retrieval and manipulation are performed by navigating through the tree structure, following the appropriate links.

  While the hierarchical model was widely used in early database systems, it has several limitations, such as limited flexibility in representing complex relationships and difficulties in modifying the structure as data requirements change.

- **Network data model**
  The network data model is an extension of the hierarchical model, allowing more complex relationships between entities. In this model, data is organized into sets of records, and each record can be associated with multiple parent or child records, forming a graph-like structure.

  The network model introduces the concept of "set" or "owner-member" relationships, where a record can be an owner of one or more member records, and a member record can belong to multiple owner records. This allows for more flexible and efficient representation of complex relationships between entities.

  However, the network model can be more complex to design and manage compared to other models, and it requires specialized tools and techniques for data manipulation and navigation.

- **Relational data model**
  The relational data model is the most widely used and widely adopted data model in modern database systems. It organizes data into tables (relations), where each table consists of rows (tuples) and columns (attributes).

  In the relational model, data is represented as a collection of relations, and each relation is defined by a set of attributes. The relationships between tables are established through the use of primary keys and foreign keys, allowing data to be stored and retrieved efficiently.

  The relational model is based on the principles of relational algebra and uses Structured Query Language (SQL) for data manipulation and querying. It provides a simple and intuitive way to represent and manage data, while also ensuring data integrity and consistency through the use of normalization techniques.

- **Object-oriented data model**
  The object-oriented data model is based on the concepts of object-oriented programming (OOP), where data is represented as objects with attributes and methods. This model is particularly useful for applications that require complex data structures and relationships.

  In the object-oriented model, data is organized into objects that encapsulate both data (attributes) and behavior (methods). Objects can inherit properties and methods from other objects, forming a hierarchy of classes and subclasses. Relationships between objects are established through associations, such as one-to-one, one-to-many, or many-to-many relationships.

  Object-oriented databases (OODBs) are designed to store and manage objects directly, without the need for mapping between object-oriented programming languages and traditional relational databases.

- **NoSQL data models**
  NoSQL (Not only SQL) databases employ various data models that are different from the traditional relational model. These data models are designed to handle large volumes of unstructured or semi-structured data, provide better scalability and performance, and accommodate changing data requirements more easily.

  - **Key-value data model**: In this model, data is stored as key-value pairs, where the key is used to retrieve the corresponding value. Key-value stores are highly partitionable and provide excellent performance for simple read and write operations. Examples include Redis and Memcached.

  - **Document data model**: Document databases store data in semi-structured documents, typically in a format like JSON or XML. Documents can have nested structures, allowing for flexible and schema-less data storage. Examples include MongoDB and Couchbase.

  - **Column-family data model**: Also known as the wide-column store model, this model stores data in column families, which are collections of columns that are logically related. It is particularly well-suited for storing and querying large amounts of data with high write throughput. Examples include Cassandra and HBase.

  - **Graph data model**: Graph databases represent data as nodes (entities) and edges (relationships between entities), making them well-suited for handling highly interconnected data and complex relationships. Examples include Neo4j and ArangoDB.

Each data model has its strengths and weaknesses, and the choice of model depends on the specific requirements of the application, such as the nature of the data, scalability needs, performance considerations, and the types of queries and operations that need to be performed.

## Relational Database Concepts

- **Tables, rows, and columns**
  In a relational database, data is organized into tables, which are two-dimensional structures consisting of rows and columns. Each table represents a specific entity or concept, and its structure is defined by a set of columns that represent the attributes or characteristics of that entity.

  - **Rows** (also known as tuples or records) represent individual instances or occurrences of the entity. Each row contains a unique set of values for the attributes defined by the columns.
  - **Columns** (also known as fields or attributes) define the types of data that can be stored in each row. Each column has a specific data type (e.g., integer, string, date, etc.) and may have additional constraints or rules applied to it.

- **Data types**
  Relational databases support a variety of data types to store different kinds of data. Common data types include:
  - Numeric types (e.g., integer, decimal, float)
  - Character types (e.g., char, varchar, text)
  - Date and time types (e.g., date, time, timestamp)
  - Boolean type (true/false)
  - Binary data types (e.g., blob, varbinary)

  Choosing the appropriate data type is crucial for efficient storage, data integrity, and performance optimization.

- **Keys**
  Keys are used to uniquely identify rows or establish relationships between tables. The main types of keys in relational databases are:

  - **Primary key**: A column or a combination of columns that uniquely identifies each row in a table. Primary keys enforce entity integrity and ensure that no duplicate rows exist.
  - **Foreign key**: A column or a combination of columns that references the primary key of another table. Foreign keys are used to establish relationships between tables and enforce referential integrity.
  - **Candidate key**: A column or a combination of columns that can uniquely identify each row in a table. A table may have multiple candidate keys, and one of them is designated as the primary key.
  - **Composite key**: A primary key or candidate key that consists of two or more columns combined.

- **Relationships**
  Relationships in relational databases define how tables are related to each other based on their keys. The three main types of relationships are:

  - **One-to-one**: A single row in one table is related to a single row in another table. For example, one employee has one employee record.
  - **One-to-many**: A single row in one table is related to multiple rows in another table. For example, one department can have multiple employees.
  - **Many-to-many**: Multiple rows in one table are related to multiple rows in another table. This type of relationship is typically implemented using a junction or associative table. For example, students can enroll in multiple courses, and courses can have multiple students enrolled.

- **Normalization**
  Normalization is the process of organizing data in a database to reduce redundancy, eliminate anomalies (insert, update, and delete anomalies), and ensure data integrity. The main normal forms are:

  - **First Normal Form (1NF)**: A table is in 1NF if it has no repeating groups of data and all entries in a column are of the same data type.
  - **Second Normal Form (2NF)**: A table is in 2NF if it is in 1NF and all non-key attributes are fully dependent on the entire primary key.
  - **Third Normal Form (3NF)**: A table is in 3NF if it is in 2NF and all non-key attributes are mutually independent (i.e., no transitive dependencies).
  - **Boyce-Codd Normal Form (BCNF)**: A table is in BCNF if it is in 3NF and every determinant (a column or set of columns on which other columns are functionally dependent) is a candidate key.

  Normalization helps to minimize data redundancy, improve data integrity, and ensure efficient storage and retrieval of data.

- **Integrity constraints**
  Integrity constraints are rules or conditions that are enforced by the database management system (DBMS) to maintain data integrity and consistency. The main types of integrity constraints are:

  - **Entity integrity**: Ensures that every row in a table is uniquely identifiable by its primary key, and primary key values cannot be null.
  - **Referential integrity**: Ensures that foreign key values in one table reference existing primary key values in another table, maintaining the relationships between tables.
  - **Domain integrity**: Ensures that data values in a column adhere to the specified data type and any additional constraints (e.g., range, pattern, or allowed values).

  Integrity constraints help to prevent data inconsistencies and maintain the overall integrity of the database.

## Database Management Systems (DBMS)
- **What is a DBMS?**
  - A DBMS is a software system designed to manage and interact with databases, providing mechanisms for creating, modifying, and querying data.
- **Types of DBMS**
  - Relational DBMS (e.g., MySQL, PostgreSQL, Oracle, SQL Server)
  - NoSQL DBMS (e.g., MongoDB, Cassandra, Redis, Neo4j)
  - In-memory DBMS (e.g., Redis, Memcached)
  - Cloud DBMS (e.g., Amazon RDS, Google Cloud SQL, Azure SQL Database)
- **Popular DBMS examples**
  - MySQL: Open-source relational DBMS, known for its simplicity and performance.
  - PostgreSQL: Open-source relational DBMS, known for its robustness and advanced features.
  - Oracle: Commercial relational DBMS, widely used in enterprise environments.
  - SQL Server: Commercial relational DBMS developed by Microsoft.
  - MongoDB: Open-source NoSQL document database, known for its flexibility and scalability.
  - Cassandra: Open-source NoSQL column-family database, designed for high availability and scalability.
  - Redis: Open-source NoSQL key-value store, often used as an in-memory cache.
  - Neo4j: Open-source NoSQL graph database, suitable for managing complex, interconnected data.

## Structured Query Language (SQL)
- **Introduction to SQL**
  - SQL (Structured Query Language) is the standard programming language for managing and manipulating relational databases.
  - It provides a consistent and intuitive way to interact with databases, regardless of the underlying DBMS.
- **SQL syntax and statements**
  - Data Definition Language (DDL): Used to create, modify, and delete database objects like tables, views, and indexes (e.g., CREATE, ALTER, DROP).
  - Data Manipulation Language (DML): Used to insert, update, and delete data in tables (e.g., INSERT, UPDATE, DELETE).
  - Data Control Language (DCL): Used to manage user access and permissions (e.g., GRANT, REVOKE).
  - Transaction Control Language (TCL): Used to manage transactions (e.g., BEGIN, COMMIT, ROLLBACK).
- **Creating, modifying, and dropping database objects**
  - Creating tables, views, indexes, and other database objects using CREATE statements.
  - Modifying the structure of existing objects using ALTER statements.
  - Dropping (deleting) database objects using DROP statements.
- **Querying data**
  - SELECT statement: Used to retrieve data from one or more tables, with various clauses for filtering, sorting, and grouping results (e.g., WHERE, JOIN, GROUP BY, HAVING, ORDER BY).
  - JOIN operations: Used to combine rows from multiple tables based on related columns (e.g., INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL OUTER JOIN).
- **Updating and deleting data**
  - UPDATE statement: Used to modify existing data in a table based on specified conditions.
  - DELETE statement: Used to remove rows from a table based on specified conditions.
- **Advanced SQL concepts**
  - Subqueries: Queries nested within other queries, enabling complex data retrieval and manipulation.
  - Views: Virtual tables based on the result of a stored query, providing a logical abstraction of data.
  - Stored procedures: Reusable sets of SQL statements that can be executed with parameters, enabling modularization and encapsulation.
  - Triggers: Special types of stored procedures that automatically execute when specific events occur (e.g., INSERT, UPDATE, DELETE).

## Database Design
- **Database design process**
  - Requirements gathering: Understanding the business requirements and data needs.
  - Conceptual design: Creating a high-level representation of the data and relationships using an Entity-Relationship (ER) model.
  - Logical design: Translating the conceptual model into a logical database schema, normalizing tables, and defining data types and constraints.
  - Physical design: Implementing the logical design in a specific DBMS, considering performance, storage, and scalability requirements.
