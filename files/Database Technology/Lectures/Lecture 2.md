## Relational Databases
---
What are Relational Databases?
<hr style="margin-top: 8px">

**Relational Databases** = A type of DBMS using the relational data model with a set of standard features:

- Strict upfront data model
- Control redundancy (storing data multiple times)
- Data **normalization** 
- Data **consistency** & integrity **constraints**
- A powerful query language (SQL)
- **Transactions** (safe simultaneous multi-access to database)
- Effective and secure **data sharing**
- **Backup** and **recovery**

## Towards Data Modelling
---
**Planning** and **developing** $\Rightarrow$ traditionally a SWE problem
- Requirements Engineering
- Conceptual Design

**Software engineers** and **data engineers** cooperate tightly in planning the need, use and flow of data.

## Towards Schema Design
---

**Data Modelling** = modelling the data requirements of a **miniworld** into a formal representation

**Requirements Analysis** = what kind of data is needed according to users & stakeholders.

**Functional Analysis** = describing high-level user operations and transactions (no implementation details yet)

---
**Conceptual Design**
<hr style="margin-top: 8px">

Transforms data requirements to **conceptual schema**
- Describes high-level data **entities**, **relationships**, **constraints** etc.

---
**Logical Design**
<hr style="margin-top: 8px">

Maps conceptual schema to the data model used by the DBMS
- Relational Model, Document Model, etc..

---
**Physical Design**
<hr style="margin-top: 8px">

Designs the internal structures needed to efficiently store/manage data.

## Generic Data Modelling
---
**Thing/Entity**
- A separate and distinct individual quality, fact, idea, or usually entity.

**Object** (Objective Entity, Definite Entity)
- Something physical, maybe perceived by senses.

**Concept** (Conceptual Entity)
- More abstract, a thought or notion

**Sets**: Collection of entitites
- Entities can be members of multiple sets
- Sets are defined in different ways (naming, selection, enumeration)
- Destroying the notion of a set does usually not destroy the set itself.

**Type**: Something that designates a set (members share some properties)
- Also "kind" or "class"
- `Students` could describe the set of all/some entities which are students

**Relationship**: A connection between two things

## Naming Conventions
---
**Data Model (theory)** = abstract model that describes how data is represented and manipulated.
- e.g. network model, relational model, object-oriented model, document-centric model.

**Data Model (instance)** = applies a data model (theory) to create a specific database.

## ER Diagrams
---
**ER Modelling** 
- **Peter Chen** introduced ER since **1976**
- Traditional approach to **Conceptual Design**
- Also known as **Entity-Relationship Diagrams (ERD)**

---
**Entity Types**
<hr style="margin-top: 8px">

= Classes of objects that have common properties:
- Examples: `CITY`, `DEPARTMENT`, `EMPLOYEE`, etc...
- Objects: occurrences of entity types

---
**Relationship Types**
<hr style="margin-top: 8px">

= Logical links between two or more entity types

An entity type is said to "participate" in a relations

