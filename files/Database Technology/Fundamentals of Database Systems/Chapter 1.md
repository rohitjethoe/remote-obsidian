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

A **database management system (DBMS)** is used for **defining**, **constructing**, **manipulating**, and **sharing** databases

- **Defining** = specifying data types, structures and constraints of the data
	- The database definition or descriptive information is also stored by the DBMS and is called **meta-data**.

- **Constructing** = storing the data on some storage medium that is controlled by the DBMS.

- **Manipulating** = querying the database to retrieve and update data or generating reports from the data.

- **Sharing** = allowing (multiple) users and programs to access the database.

**Application programs** access the database by sending queries. A **transaction** may cause some data to be read and some data to be written

