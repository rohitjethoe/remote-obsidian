*Introduction to Database Systems*

~ **5 ECTS:** 140 hours of work to pass
- 18 hours per week

DIKW Pyramid (Data, Information, Knowledge, Wisdom)

"Typically, **information** is defined in terms of **data**, **knowledge** in terms of **information**, and **wisdom** in terms of **knowledge**".

![[Screenshot 2025-11-11 at 13.37.32.png]]

- **Data** = anything (raw facts, symbols, sensor data) without any context
- **Information** = structured data with context

**Information Theory:** Lower uncertainty of the state of the world (decrease of entropy)

- **Knowledge** = understanding of information
- **Wisdom** = using knowledge to make good decisions

Initially TU Delft was a **Civil Engineering** school

**Claim 1:** A deep learning system will be just as smart as the data it gets
**Claim 2:** A deep learning system will be just as smart as the objective it optimizes

---
*Into Databases*

Data Management is the oldest topic in Computer Science.

Oracle's definition of a database:
- A database doesn't have to be in a computer system, it can be **offline**.
- A database is usually controlled by a **database management system (DBMS).** 
- A database (system) = the data, the DBMS and applications associated with them.

Database Technology: focus on how to USE databases:
- Week 1: **Database Modelling**
- Week 2: **SQL**
- Week 3: **Intermediate SQL**
- Week 4: **Relational Model, Functional Dependencies & Normalizations**

A **data model** (theory) = defines how I structure and interact with data.

"data model" is ambigious, besides theory there is also **instance** or **schema**.

There are several common data models
- **Relational Model** (which we are using)
- Key-value model
- Document-centered model
- Graph model
- And more...

Relational Model: we store data in tables
- Columns are **attributes**
- Rows are **tuples**
- **Primary Key:** is an attribute value that uniquely identifies each row

JSON is an example of the Document Model
- Redundant information
- Less flexible
- Easy global distribution

Schemas abstract the data to be stored about the real world.
- **Conceptual Schema:** What entities & relationships?
- **Logical Schema:** Transforms conceptual schema with respect to chosen data model

![[Screenshot 2025-11-11 at 16.24.14.png]]

Informal summary:
- **Database**: A collection of related data represented (using a data model and a defined data schema)
- **Database Management System (DBMS**): A software system to manage and maintain databases
- **Data Model**: Defines how to represent data (in general) and the available data operations (relational, key-value, document-centered model etc...)
- **Data Schema**: Defines the structure of a specific database

**ER Diagram** (Entity-Relationship) = Shows the entity (types) and their relationship (types).

Chen-style ER diagrams use:
- Circles for **attributes**
- Boxes for **entities**
- Diamonds for **relationships**