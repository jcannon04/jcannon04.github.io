## What is a Schema?
A database schema is a logical blueprint or structural representation of the entire database. It defines the organization, structure, and format of data stored in a database system. The schema specifies the tables, their columns, data types, constraints, relationships, and other properties that define the database's structure.

## Why do we use Database Schemas?
Database schemas are used for several reasons:

**Data Organization:** Schemas help organize data into tables and define relationships between tables, providing a structured way to store and access information.

**Data Integrity:** Schemas enforce rules and constraints on data, ensuring data accuracy and preventing inconsistencies.

**Security:** Schemas can control access to the database objects, allowing different users or user groups to have specific permissions.

**Maintenance:** Schemas provide a foundation for database maintenance and future updates, allowing changes to be made more efficiently.

### What do they look like?
A database schema is typically represented using SQL (Structured Query Language) or a database modeling language like Entity-Relationship Diagrams (ERD).

In SQL, a simple example of a schema for a table might look like this:

```
CREATE TABLE users (
    id INT PRIMARY KEY,
    username VARCHAR(50) NOT NULL,
    email VARCHAR(100) UNIQUE,
    age INT
);
```

### What are the different types of Database Keys?
In the context of database design, there are three primary types of keys:

**Primary Key (PK):** A primary key is a unique identifier for each record in a table. It ensures that each row can be uniquely identified and helps maintain data integrity. A table can have only one primary key, and it cannot contain NULL values.

**Foreign Key (FK):** A foreign key is a column (or a set of columns) in one table that refers to the primary key in another table. It establishes a link between the data in two tables, creating a relationship between them.

**Composite Key:** A composite key is a primary key that consists of multiple columns. Together, these columns create a unique identifier for each row in the table.

**What is a Primary Key?**
A primary key is a unique identifier for each record (row) in a table. It serves as the main point of reference to access and manage data in the table. The primary key enforces data uniqueness and not-null constraints for the designated column(s). Typically, the primary key is used as the basis for defining relationships with other tables through foreign keys.

**What is a Foreign Key?**
A foreign key is a column (or set of columns) in a table that refers to the primary key of another table. It establishes a link between the data in two tables, creating a relationship between them. The foreign key constraint ensures that values in the referencing column(s) must exist in the referenced table's primary key column.

**What is a Composite Key?**
A composite key is a primary key that consists of two or more columns in a table. Together, these columns create a unique identifier for each row in the table. Unlike a regular primary key, which uses a single column, a composite key uses multiple columns to uniquely identify records.

**How are they different? When do you use one over the others?**
The key differences between the three types of keys can be summarized as follows:

**Primary Key:** Used to uniquely identify records within a single table. It ensures data integrity by enforcing data uniqueness and not-null constraints. Each table can have only one primary key.

**Foreign Key:** Used to establish relationships between tables. It refers to the primary key of another table, creating a link between the two. Foreign keys are used to maintain data consistency and enforce referential integrity.

((Composite Key:)) A type of primary key that uses multiple columns to uniquely identify records. It is used when a single column cannot guarantee uniqueness, but the combination of multiple columns can.

**When to use one over the others depends on the specific requirements of your database design:**

Primary keys are fundamental and used in every table to ensure uniqueness and identification of records.

Foreign keys are used to establish relationships between tables when you need to link data from different tables based on shared information.

Composite keys are used when you need to create a unique identifier for records that cannot be achieved with a single column. They are suitable when combinations of columns are expected to be unique together.

Choosing the appropriate key type is crucial to ensuring data integrity and efficient data retrieval in a relational database. Each type of key serves a specific purpose and should be used accordingly based on the relationships and uniqueness requirements in your data model.