---
title: Week 1 - Introduction to Database and DBMS
description: ""
date: 2023-01-08T22:27:10.795Z
preview: ""
draft: false
tags: ""
categories: ""
lastmod: 2023-01-08T23:22:41.403Z
---
# Introduction to Database and DBMS
## Data, Info, Knowledge, Wisdom
- Data
	- Data is a collection of points with no discernible meaning
	- pure and simple fact
- Information
	- Information is data that is in some sort of structure and in context
	- Has meaning
- Knowledge
	- Information the has been assimilated in the mind
	- knowledge is to use data to strategically forward ones objective
- Wisdom
	- the application of knowledge
	- capacity to choose objectives that consist of ones value

## Data Bases
### What is database?
- Shared, integrated computer structure that houses:
	- End user data (raw facts)
	- Metadata (data about data)
- Data that is held in a computer usually associated with a software that is used to update and create data

### Database Systems
- A database system consists of:
	- Data (the database)
	- Software
	- Hardware
	- Users
	
Databases allows users to store, update, retrieve, organise, and protect their data

### Database Users
- End users
	- Uses the database to achieve some goals
- Application Developers
	- Writes software that allows the end user to interface with the database system
- Database administrator (DBA)
	- Create or modify the schema
	- Define and mange database system
	- Responsible for the structure of the database
	- and how it is stored
- Database systems programmer
	- Writes the database software itself

### Uses of Databases
- Databases for Businesses
- Databases for Education
- Databases for Non-profits
- Databases for Household and family management
- Everyday uses for databases

### Database management systems (DBMS)
- Collection of programs that manages database structure and controls access to data
- Makes database management more efficient and effective


#### Advantages of a DBMS
- Solve many of the problems encountered in data management
	- *e.g.*
	- Data sharing
	- Increases data security
	- Meta data integration
	- Minimise data inconsistency
	- improve data access
	- improve decision making and end user productivity
- Solves File based systems limitations

### File Based Systems (FBS)
- Data is stored in files
- Each file has a specific format
- Programs that use these files depend on knowledge about that format

#### Disadvantages of FBS
- No standards
- Data duplication
- Dependencies
- Data inconsistencies
- Limited sharing
- No way to generate ADHOC queries
- No prevision for security, recovery, concurrency

### Data Models
- A **data model** is a collection of concepts for describing data
- A **schema** is a description of a particular collection of data using a given data model
- The **relational model of data** is the most widely used model today
	- Main concept: **Relation**, basically a table with rows and columns
	- Every relation has a **schema**, which describes the columns or fields

#### Levels of abstraction
- Many **views, single conceptual (logical) schema** and **physical schema**.
- **Schemas** are defined using **Data Definition Language** (DDL)
- **Data** is modified using **Data Manipulation Language** (DML)

##### View level 
- What application programs see; views can also hide information(such as an instructor's salary) for security purposes
- Different users will see different information depending on what they are logged in as and what view has been selected for that user

##### Conceptual Level
- How the data is actually stored and structured
- Based on the data model used
- Like a blueprint of the data

##### Physical Level
- Describes how a recorded is stored
- Actual location of the data

![](/Year%201/Architecture%20%26%20Operating%20Systems/Photos/Pasted%20image%2020220603202332.png)

#### Types of data models:
- Hierarchical Model
	- First to be introduced
	- Stores data in a hierarchical data structure
	- Starts at the root and branches down into children
- Network Model
	- Extension of a hierarchical model
	- Same as the Hierarchical model apart from a few things
	- A child can have more than one parent 
	- Replaces the hierarchical tree with a graph
- Relational Model
	- Most widely used model now
	- 2 dimensional table
	- All information stored in rows and columns
- Object-oriented Data model
	- Data and relationship are stored in one object
	- Can store audio video images.
- Entity-relationship model
	- High level data model diagram
	- Real world problem is viewed in pictorial form
	- Easy to understand
- NoSQL
	- Not only SQL
	- Provides a flexible schema for the storage, retrieval of data beyond the typical table data structure found in the normal data base structures
	- Most companies use NoSQL as a data model


#### Examples of DBMS
- MongoDB - NoSQL 
- MySQL - Relational Model
- Oracle Database - Object-oriented data model
- PostgreSQL - Relational Model

*Put Notes Here*


## Videos:
- [Lecture 1](https://moodle.port.ac.uk/pluginfile.php/2667696/mod_resource/content/1/Lecture%201.mp4)
