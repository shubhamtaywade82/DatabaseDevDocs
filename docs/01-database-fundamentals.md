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
  - Data is organized in a tree-like structure, with a single root node and child nodes representing subordinate data.
  - Useful for representing data with a strict parent-child relationship, but lacks flexibility and can be challenging to modify.
- **Network data model**
  - Data is organized in a graph-like structure, with records connected to multiple parent and child records.
  - Provides more flexibility than the hierarchical model but can be complex to manage.
- **Relational data model**
  - Data is organized into tables (relations) with rows (tuples) and columns (attributes).
  - Tables are linked through shared key values, enabling efficient data storage and retrieval.
  - The most widely used data model for modern database systems.
- **Object-oriented data model**
  - Data is represented as objects, with attributes and methods, following the principles of object-oriented programming.
  - Useful for applications that require complex data structures and relationships.
- **NoSQL data models**
  - Key-value: Data is stored as key-value pairs, suitable for simple data structures and fast retrieval.
  - Document: Data is stored in semi-structured, flexible documents, suitable for storing complex, hierarchical data.
  - Column-family: Data is stored in column families, providing efficient storage and retrieval for large datasets with high write throughput.
  - Graph: Data is represented as nodes (entities) and edges (relationships), suitable for complex, interconnected data structures.

## Relational Database Concepts
- **Tables, rows, and columns**
  - Tables are used to store data, with each table representing a specific entity or concept.
  - Rows (tuples) represent individual records or instances of the entity.
  - Columns (attributes) represent the different properties or characteristics of the entity.
- **Data types**
  - Databases support various data types (e.g., numeric, string, date, time, boolean) to store different kinds of data.
  - Choosing the appropriate data type is crucial for efficient storage and data integrity.
- **Keys**
  - Primary key: A unique identifier for each row in a table, ensuring entity integrity.
  - Foreign key: A reference to a primary key in another table, establishing relationships between tables.
  - Candidate key: A column or set of columns that can uniquely identify a row in a table.
  - Composite key: A primary key composed of multiple columns.
- **Relationships**
  - One-to-one: A single record in one table is related to a single record in another table.
  - One-to-many: A single record in one table is related to multiple records in another table.
  - Many-to-many: Multiple records in one table are related to multiple records in another table, typically implemented using a junction table.
- **Normalization**
  - First Normal Form (1NF): Eliminates repeating groups and ensures atomic values in columns.
  - Second Normal Form (2NF): Eliminates partial dependencies by removing non-key attributes that depend on part of the primary key.
  - Third Normal Form (3NF): Eliminates transitive dependencies by removing non-key attributes that depend on other non-key attributes.
  - Boyce-Codd Normal Form (BCNF): Eliminates all remaining anomalies by ensuring that every determinant is a candidate key.
- **Integrity constraints**
  - Entity integrity: Ensures that every row in a table is uniquely identifiable by its primary key.
  - Referential integrity: Ensures that foreign key values reference existing primary key values in the related table.
  - Domain integrity: Ensures that data values in a column adhere to the specified data type and constraints.

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
