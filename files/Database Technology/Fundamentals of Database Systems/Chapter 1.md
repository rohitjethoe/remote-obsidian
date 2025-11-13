*Database and Database Users*

**Traditional Database Applications** = information that is stored and accessed is either textual or numeric.

**Big data storage/NOSQL systems** = manages data for social media application (huge databases for nontraditional data)

**Big data storage systems** are used by companies such as Google, Amazon and Yahoo to:

1. Manage data for Web Search engines
2. Provide **cloud storage**

**Cloud storage** = users can store all types of data on the Web.

Other types of database applications:

| Type                                                    | Used for?                                      |
| ------------------------------------------------------- | ---------------------------------------------- |
| Multimedia databases                                    | storing images, audio, video streams           |
| Geographic Information Systems (GISs)                   | analyse maps, weather data, satellite images   |
| Data warehouses and online analytical processing (OLAP) | extract and analyse business information       |
| Real-time and active database technology                | control industrial and manufacturing processes |
| Database search techniques                              | improve searching for information              |

## 1.1: Introduction
---
A **database** = a collection of related data.

By **data**, we mean:
- known facts that can be recorded,
- and have implicit meaning

A database has the following implicit properties: 
1. **Miniworld:** It represents some aspect of the real world
2. **Logically coherent collection of data with some meaning:** 
	- A random assortment of data is NOT a database.
3. **Specific purpose**: is **designed**, **built** and **populated** with data for **a specific purpose** 

A **database management system (DBMS)** is used for **defining**, **constructing**, **manipulating**, and **sharing**, **protecting** and **maintaining** databases

1. **Defining** = specifying data types, structures and constraints of the data
	- The database definition or descriptive information is also stored by the DBMS and is called **meta-data**.
2. **Constructing** = storing the data on some storage medium that is controlled by the DBMS.
3. **Manipulating** = querying the database to retrieve and update data or generating reports from the data.
4. **Sharing** = allowing (multiple) users and programs to access the database.
5. **Protection**:
	- **System protection** against hardware or software malfunction
	- **Security protection** against unauthorized or malicious access
6. **Maintaining** = allowing the system to evolve as requirements change over time

**Application programs** access the database by sending queries. A **transaction** may cause some data to be read and some data to be written

It is also possible to create a **special-purpose DBMS software**

A **database system** = DBMS software and the database together.

## 1.2: An Example
---
![[Screenshot 2025-11-12 at 14.11.22.png]]

### **`UNIVERSITY` database**: 

*Stores five **data records** of the same type.*
- The **`STUDENT`** file stores data on each student
- The **`COURSE`** file stores data on each course
- The **`SECTION`** file stores data on each section of a course
- The **`GRADE_REPORT`** file stores the grades that students receive in courses they have completed
- The **`PREREQUISITE`** file stores the prerequisites of each course

To **define** this database we specify the different types of **data elements** to be stored in each record

We must also specify a **data type** for each **data element**
- **`Student_Name`** is a string of alphabetic characters
- **`Student_Number`** is an integer
- **`Student_Class`** could use an encoding scheme e.g. '1' for 'freshman'

To **construct** the database we store data to represent each `STUDENT`, `COURSE`, `SECTION`, `GRADE_REPORT` etc... 

Database **manipulation** involves **querying** and **updating data.**
- Queries are specified in the query language of the DBMS

The database is part of a larger undertaking known as an **information system within an organization**.

Designing new database applications or new databases is done in phases:
1. **Requirements specification and analysis**: requirement documentation
2. **Conceptual design**: 
	- Represented and manipulated using computerized software
	- Can be maintained, modified and transformed into a database implementation
3. **Logical design**: expressed in a data model implemented in a commercial DBMS
4. **Physical design**: actual implementation, populated with actual data and maintained to reflect the miniworld

## 1.3 Characteristics of the Database Approach
---
Older approach before databases is **traditional file processing**
- **Grade report office:** keeps files on students and their grades
- **Accounting office**: keeps files on students fees and their payments

**Downsides** of traditional file processing:
- Redundant in defining and storing data 
- Wastes storage space
- Redundant in maintaining common up-to-date data

In the **database approach** a single DB maintains data that is defined once and accessed by various users through **queries**, **transactions**, and **application programs**.

**Database approach vs traditional file processing:**
- Self-describing nature of a database system
- Insulation between programs and data, and data abstraction
- Support of multiple views of the data
- Sharing of data and multiuser transaction processing

### 1.3.1: Self-Describing Nature of a Database System
---
A database system contains **a complete definition of the database structure and constraints**.

**Meta-data** = describes the structure of the primary database.

NOSQL systems do not require meta-data. Rather the data is stored as **self-describing data**.

Data definition in **traditional file processing** is usually part of the application programs themselves. This constrains the programs to work with only specific databases.

DBMS software can access diverse databases by extracting the DB definitions from the catalog.

### 1.3.2: Insulation between Programs and Data, and Data Abstraction
---
**Program-data independence** = access programs and the DBMS catalog are stored separately.

X.................

### 1.3.3: Support of Multiple Views of the Data
---
A database has many types of users where each may require a different **view** of the database.

A **view** might be a subset of the DB or it may contain **virtual data** that is derived from the DB files but not explicitly stored.

### 1.3.4: Sharing of Data and Multiuser Transaction Processing
---
**Concurrency control software** = updating the same data in a controlled manner so that the result is correct.

**Online transaction processing (OLTP)** = application to ensure concurrent transactions operate correctly and efficiently

**Transaction** = executing program or process that includes one or more database accesses.

