---
title: Week 2 - Relational Model , Entity Relationship Diagram
description: ""
date: 2023-01-08T22:28:03.422Z
preview: ""
draft: false
tags: ""
categories: ""
lastmod: 2023-01-08T23:23:16.114Z
---
# Relational Model , Entity Relationship Diagram

## Definitions
- Relational database: A Set of relations
- Relation: Made up of two parts
	- Instance
		- A table with rows and columns
	- Schema
		- Name of relation
		- name and type of each column

## The Relational Model
- The foundation for most (but not all) current database systems
- Concerned with 3 main things
	- Data structure
		- How the data is represented
	- Data integrity
		- what data is allowed
	- Data manipulation
		- What you can do with the data

### Relational Data Structure
- Data is stored in relations
	- Each relation has a scheme (The heading)
	- The scheme defines the relations attributes (The column)
	- Data take the form of tuples (The Rows)
![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220603205645.png)
### Relational Data integrity
- Data integrity is the overall completeness, accuracy and consistency of data
- Data integrity controls what data can be in a relation
	- Domains
		- The possible values a tuple can assign to an attribute
	- Candidate and Primary Keys
		- identify tuples within a relation
	- Foreign keys
		- link relations to each other

#### Attributes and Domains
- A Domain is given for each attribute
- The domain lists the possible values for that attribute
- Each Tuple assigns a value to each attribute for its domain

#### Candidate Keys
A set of attributes in a relation is called a candidate key only if:
- Every tuple has a unique value for the set of attributes (Uniqueness)
- No proper subset of the set has the uniqueness property (Minimality)

- Must contain unique values
- Must not contain NULL values
- Should contain minimum field to maintain uniqueness and uniquely identify each record in a table
- May have multiple attributes

#### Primary Keys
A Primary key is a candidate key that is usually chosen to be used to identify tuples in a relation.
Often a special ID attribute is used as the Primary key
- Two Rows cant have the same primary key
- Every row must have a primary key
- Cannot be NULL
- The value can never be updated or modified
- These rule apply to any foreign keys that link to a primary key

#### Foreign Keys
A Foreign Key is a column that creates a relationship between two tables.
A foreign key is another tables primary key thus linking them together.
- Must have a matching primary key or be NULL (Referential integrity)

#### Referential Integrity
This is a constraint that is specified between two tables (the parent and child). It maintains the correspondence between rows within these tables.

##### Options
- RESTRICT
	- Doesn't allow any user to modify any rows
- CASCADE
	- Allows changes to be made
- NULLIFY
	- Allows to make the value NULL

#### Entity Integrity
- Ensures that there is no duplicate records within the table

#### Naming conventions
- Naming conventions
	- A consistent naming convention can help to remind you of the structure
	- Assign each table with a unique prefix
- Naming Keys
	- Having a unique number as a primary key can be useful
	- If the table prefix is abc, call this abcID
	- A foreign key to this table is then also called abcID
![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220604135849.png)

## Entity Relationship Diagram (ERD)
An ERD is a type of structural diagram for use within database design.
![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220604141331.png)
You should create a ERD before creating a database so that you know exactly what is going into the database and how it is structured.

#### What to know before creating a database.
- Know how to design one.
- What tables, keys, and constraints that are needed?
- What is the database going to be used for?
- The **Entities** to be stored
- The **Relationships** to be stored
- The **Data integrity constraints** or rules to be followed

#### ER Model Basics
- Entity
	- Real-world object distinguishable from other objects.
	- An entity is described using a set of **attributes**
- Entity Set
	- A collection of similar entities
- Relationship
	- Association among two or more entities
- Relationship Set
	- Collection of similar relationships
#### Entity/Relationship Diagram
- E/R Models are often represented as an E/R diagram
	- It gives a conceptual view of the database
	- Are Independent of the choice of DBMS
	- Can identify some problems within a design
##### Entities
- An entity is a definable thing or concept within a system, such as a person/role
- In ER models, an entity is shown as a rounded rectangle, labelled with the name of the call of objects represented by that entity
- Basically the tables
![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220604141654.png)
*Entities are highlighted in blue*

##### Attributes
- AKA, the column
- It is the property or characteristic of the entity that holds it
- Drawn as ovals
- Each attribute is linked to its entity by a line
- the name of the attribute is put within the oval
  ![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220604142325.png)
*Attributes are highlighted in blue*

##### Relationships
- Signifies that two entities are somehow associated with each other
- The name is given in a diamond box
- The end of the link shows the cardinality
![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220604142552.png)
*Relationships are highlighted in blue*

###### Cardinality
- Each entity within a relationship can participate in zero, one, or more than one instance of that relationship
  ![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220604142817.png)

The ones that we need to know:
- One-to-One (1:1)
	- A One-to-One relationship is mostly used to split an entity in two to provide information concisely and make it more understandable.
- One-to-Many (1:M)
	- A One-to-Many relationship refers to the relationship between two entities X and Y in which an instance of X may be linked to many instances of Y, but an instance of Y is linked to only one instance of X
- Many-to-Many (M:M)
	- A Many-to-Many relationship refers to the relationship between two entities X and Y in which X may be linked of Y and vice versa
	- Can be split into many One-to-Many relationships (Not covered in this course)

#### Why is it important?
- it is risky to alter a database structure directly in a DBMS
- Identify the mistakes and design flaws
- easily locate entities, attributes and relationships
- Allow to analyse the database




*Put Notes Here*


### Example
Starting Information:
- Each product has a description, a price, and a supplier
- Suppliers have addresses, phone numbers, and names
- Each address is made up of a street address, a city, and a postcode

1. Place the Entities down with their attributes![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220604144058.png)
2. Connect the Entities together using relationships![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220604144156.png)


## Videos:
[Lecture 2](https://moodle.port.ac.uk/pluginfile.php/2667700/mod_resource/content/1/zoom_0.mp4)

