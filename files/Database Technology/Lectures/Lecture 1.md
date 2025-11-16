## Grading
---
- **Database**: Midterm  $\Rightarrow$ 50%
- **Web**: Endterm           $\Rightarrow$ 50%
- **Resit**: either both or individually.

## Literature DB
---
**Fundamentals of Database System** Elmasri & Navathe, 7th edition.

## Expectations
---
Web & Database Technology is a **5 ECTS** course
- About **20 hours/week**.

## Information, Data and Knowledge?
---
**Information and Data Modelling**
<hr style="margin-top: 8px">

**DIKW Pyramid:**
	**D**ata
	**I**nformation: contextualizing data
	**K**nowledge: give meaning to information
	**W**isdom: gain insight from knowledge

**Information Theory:** 
	Idea that information decreases entropy or the uncertainty on the state of the world.

---
**Deep Learning**
<hr style="margin-top: 8px">

**Deep Learning** systems will only be 
	1. As smart as the **data it gets**.
	2. As smart as the **objective it optimizes**.

Only a small fraction of real-world ML systems is ML algorithm development. A lot of effort (80%) lies into **data management**.

---
**Into Databases**
<hr style="margin-top: 8px">

- **Database** = a collection of related data (represented using a data model and data schema)
- **Database Management Systems (DBMS)** = a software managing and maintaining a database.

Why databases and not just files?
1. Data Integrity & Consistency
2. Concurrency Control
3. Querying & Flexibility
4. Scalability & Performance
5. Security & Access Control
6. Backup & Recovery

- **Tier-1 Architecture:** Applications and Database on a single local machine.
	✅ Simple Architecture
	✅ Cheap
	❌ Limited to Single User
	❌ Bad Security
	❌ No Centralized Control

- **Tier-2 Architecture:** Clients (Apps + Users) communicate over network with DB
	✅ Easy Access and Deployments
	✅ Scalable
	✅ Low Cost
	❌ Security Issues
	❌ Difficult Maintenance
	❌ Limited Scalability

---
**CSE1500 Overview**
<hr style="margin-top: 8px">

**Week 1**:
 *(1) Introduction to Database Systems*
 *(2) Introduction to Modelling*

-**Week 2**:
 *(3) Jumpstart SQL Query Language*
 *(4): Introduction to Modelling (part 2)*

**Week 3**:
 *(5): Intermediate SQL Query Language*
 *(6): Data Models & The Relational Model*

**Week 4**:
 *(7): The Relational Model, Functional Dependencies & Normalizations*
 *(8): Roundup Q&A*

---
**Towards Modelling**
<hr style="margin-top: 8px">

- **Data Model** = A general definition on how to represent data and the available data operations
- **Data Schema** = A definition of the structure of a specific database

**Conceptual Schema**: Describes all entity types & relationships
- **Entity Type**: A type of thing existing in the real world
- **Relationships**: Connections between entities

**ER Diagram** = Visual representation of entities and their relationships

A data models consist of 3 parts:
1. **Structure**: Data Structures used to create and represent databases 
2. **Integrity**: Rules expressing **constraints** on these data structures 
3. **Manipulation**: Operations that can be applied to the data structures (query/update)

---
**Relational Data Model**
<hr style="margin-top: 8px">

**Relational Data Model** = uses multiple data tables that have relationships.
- Every **entity type** & **relationship type** has it's own table

**✅ Pro's of Relational DB's:**
  Very expressive
  Flexible & fast query language	

**❌ Cons of Relational DB's:**
  Requires DBMS to manage, maintain and update
  Complex to use
  Complex to design

---
**Single-Table Model**
<hr style="margin-top: 8px">

**Single-Table Model** = represents all data as a single table
- Typically by representing as a `.csv` or Excel file

**✅ Pro's of Single-Table DB's:**
  Very simple
  Can easily be converted to files
  No DBMS necessary

**❌ Cons of Single-Table DB's:**
  Hard to perform queries
  Schema is flattened (most conceptual schema information is lost)
  A lot of data redundancy depending on flattening

---
**Document Model**
<hr style="margin-top: 8px">

**Document Model** = uses a semi-structured text document tree (like `.json` or `.xml`)

**✅ Pro's of Document DB's:**
  Can be converted to files
  No DBMS needed
  Very scalable and distributable

**❌ Cons of Document DB's:**
  Less powerful queries
  Some data redundancy

