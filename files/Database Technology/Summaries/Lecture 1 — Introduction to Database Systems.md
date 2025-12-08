---
date: 2025-11-20
title: Introduction to Database Systems
tags:
  - CSE1500
---
**Table of Contents**:
- [[#Lecture Slides]]
- [[#Ch. 1 Introduction to Databases]]

![[WDT01_Introduction.pdf]]
## Lecture Slides
---
**Information, Data and Knowledge**
****
- **Data** = raw, unprocessed facts
	- Observations
	- Symbols
	- Signals
- **Information** = data that has been structured or contextualised
- **Knowledge** = information interpreted through experience or expertise
- **Wisdom** = knowing the right thing to do

---
**Artificial Intelligence**
****
- A deep learning model is only as good as:
	1. **the data it gets.**
	2. **the objective it optimizes.**

**Data management** is foundational in creating deep learning systems.

---
**Into Databases**
****
- **Database** = a collection of related data represented using a data model and a defined data schema.
- **Database Management System (DBMS)** = a software system managing and maintaining a database.

1. **Data Integrity & Concurrency**
	- Rules & constraint to ensure data stays reliable
2. **Concurrency Control**
	- Allows multiple people access data at the same time
3. **Querying & Flexibility**
	- Have languages to find and manipulate data quickly
4. **Scalability & Performance**
5. **Security & Access Control**
	- Control access, require authentication and track who did what
6. **Backup & Recovery**
	- Automated backup and tools to recover data after crashes

**Tier 1 Architecture:** apps & database on single local device.

**Tier 2 Architecture**: apps & users (client) talk to database over a network

---
**CSE 1500 Overview**
****
- **Week 1**:
	- 1.1: Introduction to Database Systems
	- 1.2: Database Modelling
- **Week 2**:
	- 2.1: Jumpstart SQL Query Language
	- 2.2: Database Modelling (part 2)
- **Week 3**:
	- 3.1: Intermediate SQL Query Language
	- 3.2: Data Models & The Relational Model
- **Week 4**:
	- 4.1: The Relational Model, Functional Dependencies & Normalizations
	- 4.2: Roundup & Q&A

---
**Towards Modelling**
****
- **Data Model** = a formal definition on how to represent data (in general) & the available data operations
- **Data Schema** = a definition of the structure of a specific database

**Conceptual Schema**: describes all entity types and relationship types
- **Entity Type**: A type of thing existing in the real world
- **Relationships**: Connections between entities

**ER Diagram** = shows entity types and their relationship types

**Logical Schema** = represents the conceptual schema in the chosen data model

****
**Relational Model** = Represents data tables which are linked (via ids and foreign keys)
****
- **Pros**:
	- Expressive
	- Flexible and fast (query language)
- **Cons**:
	- Requires a DBMS, schemas, constraints and queries
	- Complex to use
	- Complex to design

****
**Single-Table Model** = Represent all data as a single table
****
- Represented by a `.csv` or `.xlsx` file 
- Mostly used for exchanging data

- **Pros**:
	- Simple
	- Easily converted to files
	- NO DBMS necessary
- **Cons**:
	- Inflexible query language
	- Schema is flattened (conceptual schema information is lost)
	- A lot of data redundancy depending on how the schema was flattened

****
**Document Model** = Represents as semi-structured text documents
****
- Represented by `.json` or `.xml` file
- Typically: decide on a main entity type and embed all it's sub-entities in a substructure
- Queries can filter the document
- Often used in Web APIs and Web Systems

- **Pros**:
	- Simple
	- Easily converted to files
	- No DBMS necessary
	- Very scalable and distributable
- **Cons**:
	- Somewhat inflexible query language
	- Some data redundancy depending on the aggregation perspective

****
**Summary**
****
- **Databases** are collection of related data represented using a **data model** and structured using a **data schema**
	- **Conceptual Schema**: describes entities types and their relationship types
	- **Logical Schema**: represents conceptual schema in the chosen data model
- **Data model** governs how data can be represented and manipulated
	- **Relational Model**: uses tables with attributes, ids and links by foreign key constraints
	- **Single-Table Model**: one table without constraints
	- **Document Model**: uses semi-structured document tree (`.json`, `.xml`, MongoDB, etc.)


## Ch. 1 Introduction to Databases
****
**Introduction**
****
A **database**: collection of related data
- **Data**: known facts that can be recorded and have implicit meaning

**Properties of a database**:
1. Represents some aspect of the real world called the **miniworld** or **universe of discourse (UoD)**
2. Database is a logically coherent collection of data with inherent meaning
3. Database is designed, built and populated with data for a specific purpose

A database can be either **manually** or it can be **computerized**

A **database management system (DBMS)**: system that enables users to create and maintain a database
- A **DBMS** is a general-purpose software system
- A **DBMS** facilitates:
	1. **Defining** data types, structures and constraints (rules stored as **meta-data**)
	2. **Constructing** data to be stored on some storage medium controlled by the DBMS
	3. **Manipulating**: querying data and updating to reflect changes in the miniworld
	4. **Sharing**: allows multiple users and programs access simultaneously
	5. **Protection**: 
		- System protection: hardware or software crashes
		- Security protection: unauthorized access
	6. **Maintenance**: evoling the system as requirements change over time

An **application program** accesses the DB by sending queries to the DBMS

 A **query**: causes data to be retrieved
 A **transaction**: causes data to be read and data to be written 

**Database System**: the database and the DBMS software together.

****
**An Example**
****

****
**Characteristics of the Database Approach**
****
**File Processing**: Each application keeps it's own files & programs 
- Data is duplicated: wasted storage & extra work

**Database Approach**: One central repository holds data, which can be accessed by multiple users and applications
- Reduces redundancy and keeps data consistent

**Main Characteristics of Databases**
1. **Self-describing nature**:
	- A (specific) database stores structure, types and rules (**metadata**) in a catalog.
	- DBMS uses catalog to understand how to read/write data
2. **Insulation between programs and data (data abstraction)**:
	- Programs don't need to know the details of how data is stored
3. **Support for multiple views**:
	- Different users may need different **views** of the data
4. **Sharing data and multiuser transaction**:
	- Multiple users can safely access and update the DB at the same time
	- DBMS uses **transactions** to ensure data stays correct when people are working on it simultaneously.

---
**Actors on the Scene**
****
In any organization:
- **Primary resource**: database itself
- **Secondary resource**: DBMS and related software

**Database Administrators (DBA)**: Administers database and is responsible for:
- Authorizing access to the DB
- Coordinating and monitoring DB usage
- Acquiring software and hardware resources as needed

**Database Designers**: Identifies data to be stored in the database & choosing appropriate representation & storage structures

**End Users**: Databases primarily exist for their use (querying, updating and generating reports)
