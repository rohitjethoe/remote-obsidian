---
date: 2025-11-20
title: Modelling
tags:
  - CSE1500
---
![[WDT02_Engineering and DB_Modelling.pdf]]
## Lecture Slides
****
**Lecture Goals**
****
- Engineering & Computer Science
- Why Modelling?
- Introduction to Entity-Relationshop Diagrams (ER)

****
**Engineering**
****
- **Goal**: Applies scientific and technical principles to design and build solutions, assess and maintain them
- **Focus**: Systems, infrastructure, machine, processes
- **Output**: Physical or digital products that solve real-world problems
- **Mindset**: "How can I address this problem systematically, reliably and safely"

****
**Scientist**
****
- **Goal**: Expands knowledge by discovering new truths about nature, phenomena or philosophical construct
- **Focus**: Research, experimentation, theory
- **Output**: Knowledge, models and insights
- **Mindset**: "Why does this happen? What are underlying laws? How can I control this?"

****
**Programmer**
****
- **Goal**: Writes code to implement logic, automate tasks or build software
- **Focus**: Algorithms, programming languages, debugging
- **Output**: Software applications, code, scripts
- **Mindset**: "How do I make this program run?"

****
**Engineering Workflow**
****
**CDIO Initiative** = formalising engineering educations
- **Conceive**
- **Design**
- **Implement**
- **Operate**

**CDIO** not sufficient, make it **CDIAO**:
- Conceive
- Design
- Implement
- **Assess**
- Operate

****
**Schema Design**
****
**Data modelling** = modelling data requirements of a **miniworld** into a formal representation
- **Miniworld**: universe of discourse
- A restricted view on the real world with respect to problems that the application should solve

**Requirements Analysis**: 
- Database designers interview prospective **users** and **stakeholders**
- **Data Requirements**: what kind of data is needed?
- **Functional Requirements**: what kind of operations are performed on the data?

**Functional Analysis**: Describe high-level user operations and transactions

**Conceptual Schema**: describes high-level data entities, relationships and constraints
- Independent of used software & hardware
- Does not contain implementation details

**Logical Schema**: maps the conceptual schema to the data model used by the DBMS
- Relational Model, Document Model, etc...
- Depends on the data model of chosen DBMS

****
**Data Modelling**
****
A **data model (theory)** = abstract model that describes how data is represented, accesses and reasoned about

Common data models:
- Relational Model
- Key-Value Model
- Document Model
- Graph Model

A data model describes data objects, operations and their effects
- **Data Definition Language (DDL)** = how to structure data
- **Data Manipulation Language (DML)** = how to add, edit, delete data
- **DDL** and **DML** are usually clearly separated, since they handle **data** and **meta-data**

A **data model (instance)** = describes a specific miniworld (also a data schema)

****
**ER Diagrams**
****
**Entity-Relationship Diagrams (ERD)**
- Introduced in 1976 by Peter Chen
- Graphical representation for entities, attributes, relationships and constraints

ER Modelling consists of defining:
- Entity Type
- Weak Entity Type
- Attributes
- Key Attribute
- Multi-Valued Attribute
- Composite Attribute
- Derived Attribute
- Relationship Type
- Identifying Relationship Type
- Total Participation
- 1:N Cardinality

****
**Entity Types**
****
**Entity Types** = Classes of objects that have:
1. Common properties
2. Autonomous existence

An occurrence of an entity type is called an object or an entity.

****
**Relationship Types**
****
**Relationship Types** = Logical links between two or more entity types.
- Defines a set of associations between entity types
- An entity type is said to participate in a relationship

**Degree of a relationship type**
	= Numbers of participating entity types (binary, ternary, recursive)

**Cardinality**: describes maximum and minimum number of relationships in which an entity can participate
- **Maximum** (cardinality ratio):
	- **1**: each entity is associated with a single relationship.
	- **N**: each entity is associated with an arbitrary number of relationships
- **Minimum** (participation constraint):
	- **0**: participation in the relationship is optional or *partial*
	- **1**: participation in the relationship is mandatory or *total*

****
**Simple Attributes**
****
**Simple Attributes** = describes elementary properties of entity types or relationship types
- Attributes are characterised by a domain

Typically **attribute** cardinality is (1, 1):
- **Minimum cardinality 0**: value can be `NULL`
- **Maximum cardinality N**: multi-valued attribute

****
**Composite Attributes**
****
**Composite Attributes** = concatenates simple attribute types into a composite attribute
- Composite attributes can form hierarchy

****
**Derived Attributes**
****
**Derived Attributes** = attributes having values generated from other attributes
- Through calculations, algorithms or procedures

****
**Identifiers**
****
**Identifiers** (keys) = describe the unambiguous identification of entity instances
- An identifier is specified for each entity type
- Relationships have no identifier

**Internal Identifier** = identifier formed by (one or more) attributes of the entity itself
- Attribute cardinality is (1, 1)
- Each entity must have 1 identifier, but can have more
	- All distinct underlined attributes are keys
- There is no primary key in ER, only **keys**.

****
**Weak Entities**
****
**Weak Entity** = if attributes of an entity type are not sufficient to identify unambiguously

**External Identifier** = Other entities need to be involved in the identification

**Identifying Relationship** = relationship that relates a weak entity to it's owner

****
**Enhanced Entity-Relationship Diagrams (EER)**
****
**EER Diagrams** = more accurate database schemas reflecting properties and constraints more precisely
- Includes all modelling concepts of the ER model
- In addition: subclasses and superclasses

****
**Class/Subclass Relationship**
****
**Generalisation/Specialisation Relationship** = logical links between an entity $a$, known as parent entity and one or more entities $a_1, ... a_n$ called child entities
- $a$ is a **generalisation** of $a_1, ..., a_n$ 
- $a_1, ..., a_n$ is a **specialisation** of $a$

- The circle defines the entities involved in the specialisation
- The subset symbol ($\subset$) indicates the direction of the specialisation

- Instances of a **child entity** is also an instance of **parent entity**
- **Inheritance**: every property of the parent entity is also a property of a child entity
- Specialisation can define their own specific attributes or relationship types

****
**Membership**
****
**Predicate-defined (or condition-defined) subclasses** = determine exactly the entities that will become member of each subclass

**Attribute-defined subclasses** = all subclasses have their membership condition on the same attribute

**User-defined subclasses** = no specific condition
- Specialisation defined by the DB user instance by isntance