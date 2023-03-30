	2 - 1

CONCEPTUAL MODEL

is not concerned with how the Physical Model will be implemented.

Captures the functional and informational needs of a business.
 - important entities (object that become table in DB)
 - relationships among entities

 Logical model

 - Includes all entitis and relationship among them
 - Is called an entity relationship model (ERM)

PHYSICAL MODEL

is derived from the Conceptual Model.

Is an extension to a logical data model
 - Defines table definitions, data types, and precision

Show all table structures, including columns, primary keys, and foreign
keys.

Data model

is the process of capturing the important concepts and rules that shape
a business and depicting them visually on a diagram

Terminology
 - Conceptual model
 - Data
 - Data modeling
 - Physical modeling

	2 - 2

ENTITIES

They are usually a noun.

 - a nanme for a set of similar things that you can list
 - objects, events, people
 	Entities   Instances
 	- PERSON - Mahatma Gandhi
 - entities have instances

ATTRIBUTES

 - has a single value
 - an attribute is a specific piece of information that helps:
 	Describe an entity
	Quantify
	Qualify
	Classify
	Specify

 - These are called "data types" of "formats"

Entities	Attributes
CUSTOMER	family name, date of birth, ...

 - Some atributes have values that constantly change
 	- call volatile attributes
 - Other attributes will rarely change, if ever
 	- call nonvolatile attributes
 - Some attributes must contain a value
 	- call mandatory attributes
 - Other attributes may either contain a value or be left null
 	- call optional attributes

Unique Identifiers

 - UID is either a single attribute or a combination of multiple attributes
   that distinguishes one employee from another

Terminology

 - Attribute
 - Data type
 - Entity
 - Instance
 - Mandatory
 - Intangible
 - Null
 - Optional
 - Single values
 - Tangible
 - Unique identifier (UID)
 - Volatile

	2 - 3

Implementation-free
 - A good conceptual data model stays the same regardless of the type of
   DB the system is eventually build -or implemented -on

ERD (Entity relationship diagram)
 - is an example of a Logical Model.
 - is a consistent tool that can be used to represent the data
 - list of all entities and atributes as well as all relationships
   between the entities that are of importance
 - background information - entity description, data types and constraints
 - the model does not require a diagram, but is a very useful tool

 ER modeiling
  - Capture all required data
  - Ensure that data appears only once
  - Model no data that is derivable from other data already modeled
  - Locate data in a predictable, logical place

Terminology
 - Entity relationship diagram (ERD)
 - Implementation-free
 
 
	DD 3-1: IDENTIFYING RELATIONSHIPS

Identify the relationship between entities makes it easier to understand the
connections between different pieces of data

RELATIONSHIPS IN DATA MODELS

 - Represent something of significance or importance to the business
 - show how entities are related to each other
 - exist only between entities (or one entity and itself)
 - are bi-directional
 - are named at both ends
 - have optionality
 - have cardinality

Relationships are either mandatory or optional.
Cardinality measures the quantity of somethings.

	Each EMPLOYEE must hold one and only one JOB.

TERMINOLOGY
 - Cardinality
 - Optionality
 - Relationship


	DD 3-2: Diagramming Conventions

ER drawing conventions
 - Entitties
	- entities are represented by softboxes
	- entities names go in the softboxes
	- entity names are always singular and written all capital letters

 - Atributes are listed under the entity names
	- mandatory attributes: *
	- optional attributes: o
	- Unique identifiers: #

 - Relationships
 	- are lines that connect entities
	- lines are either solid or dashed (Cardinality)
	- terminate "single toe" or "crow's foot"

TERMINOLOGY
 - Softbox
 - ER Diagramming
 - Crow's Foot
 - Single Toe

 	DD 3-3: Speaking ERDish and Drawing Relationships

ERDish 	- the vocabulary used to clearly communicate the business rules
	- is the language we use to state relationships between entities in a ERD
	- identified relationships and specified optionality and cardinality 	 

THE COMPONENTS OF ERDish
 - EACH
 - Entity A
 - OPTIONALITY (must be/may be)
 - RELATIONSHIP NAME
 - CARDINALITY (one and only one/one or more)
 - Entity B

 each relations has two sides, we read the first from left to right (or top to
 bottom)

TERMINOLOGY
 - ERDish

	DD 3-4: Matrix Diagrams

 - Draw a ERD from a matrix diagram

using especially when you are dealing with many entities



DD 4-1: Supertypes and Subtypes
==============

 occur frequently in the real world:
  - payment types (check, cash, credit)

TERMINOLOGY
 - Exhaustive
 - Mutually exclusive
 - Subtype
 - Supertype

DD 4-2: Documenting Business Rules
==============

 - Structural business rules indicate the types of information to be stored
   and how the information elements interrelate
 - Pricedural rules deal with the prerequisites, steps, processes, or
   workflow requirements of a business
 - Many procedural business rules are related to time: event A must happen
   before event B
 - Structural business rules can nearly always be diagramed in the ERD
 - Some procedural business rules cannot be diagrammed, but must still be
   documented so that they can be programmed later

STRUCTURAL RULE EXAMPLE
 - Structural business rules indicate the types of information to be stored
   (attributes) and how the information elements interrelate (relationships)

 - Structural business rules can nearly always be diagrammed in the ERD

RULE DISCUSSION

PROCEDURAL RULE 

TERMINOLOGY
 - Business rule
 - Procedural business rule
 - Structural business rule

A bussiness rule such as "We only ship goods after customer have completely
paid any outstanding balances on their account" is best enforced by:

	Creating additional programming code to verify no goods are shipped 
	until the account has been settled in full.

DD Section Quiz
==============

Which of the following is true about subtypes?
 - Subtypes must be mutually exclusive

A subtype is shown on an ERD as an entity with a one to many relationship 
to the supertype. True or False?
 - False

Business rules are important to data modelers because:
 - They capture all of the needs, processes, and required functionality of the
   business
 - The data modeler must focus on structural rules, because they are easily
   represented diagrammaticaly and eliminate other rules that involve extra
   procedures or programming.


	SECTION 5 - RELATIONSHIP FUNDAMETALS
==============

DD 5-1: Relationship Transferability
==============

 - Nontransferable Relationship
 	- A nonstransferable relationship is represented with the diamond on
	  the relationship

TERMINOLOGY
 - Nontransferable
 - Transferable

A non-transferable relationship means the relations is manatory at both sides.
 False

DD 5-2: Relationship Types
==============

ONE-TO-MANY (1:M) RELATIONSHIPS

 - The various types of 1:M realationships are most common in an ER model

MANY-TO-MANY (M:M)

 - The various types of M:N relationships are common, particularly in a first
   version of an ER model
 - In later stages of the modeling process, all M:M relationships will be
   resolved, and disapper

ONE-TO-ONE RELATIONSHIPS FOR ROLES

 - Usually you will find just a few of the various types of 1:1 relationships
   in every ER model
 - Mandatory at one end of the 1:1 relationship commonly occurrs when roles
   are modeled

REDUNDANT RELATIONSHIPS

 - A redundant relationship can be derived from another relationship in the
   model

TERMINOLOGY
 - Many-to-many (M:M)
 - One-to-many (1:M)
 - One-to-one (1:1)
 - Redundant


DD 5-3: Resolving Many-to-Many Relationships
==============

 - Identify attributes which belong to many-to-many relationships
 - A third entity is needed to resolve the M:N relationship
 - This is called an "intersection" entity

INTERSECTION ENTITY

 - The original M:N relatioship has become two 1:M relatinships

BARRED RELATIONSHIPS

 - The unique (UID) of the intersection entity often comes from the originating
   relationships and is represented be the bars
 - The relationships from the originating entities to the intersection entity
   are called "barred" relationships

TERMINOLOGY
 - Barred relationships
 - Intersection entity

QUIZ

 A relationship on an ERD can have attributess.
 	False

DD 5-4: Understanding CRUD Requirements
==============

 - From the business scenarios that you develop and the list of business rules
   that you identify during client interviews, you will build the ERD
 - The ERD is the conversation tool between the consultant and the client, and
   it is also the blueprint for the DBA who will eventually build the DB
 - You need a way to check that you haven't missed any entities or relationship
   in your data model
 - You also want to make sure that you haven't modeled anything that the 
   business does not required
 - CRUD analysis will help you do this

CRUD ANALYSIS

 - is an acronym for create, retrieve, update, delete
 - these are the four basic functions (or operation) that a database allows
 - part of checking a data model for completeness and accuracy is making sure
   that all the CRUD functions specified by the business scenario and the
   business rules are represented in the ERD

	CRUD ANALYSIS - CREATE FUNCTION

 - During the client interview, and while writing the business scenarios 
   and rules, look for keywords like:
    - INPUT, ENTER, LOAD, IMPORT, RECORD, & CREATE
 - These all indicate that a record is created in the database at this time

	CRUD ANALYSIS - CREATE FUNCTION
 - During the client interview, and while writing the business scenarios and
   rules, look for keywords like:
   	- VIEW, REPORT, BRING UP, PRINT, FIND, READ, & LOOK UP
 - These all point to retrieving information from the database
 - Review the requirements for these keywords

	CRUD ANALYSIS - UPDATE FUNCTION
 - CHANGE, MODIFY, ALTER, & UPDATE
 - These all point to updating information that is already in the DB

	CRUD ANALYSIS - DELETE FUNCTION

 - DISCARD, REMOVE, TRASH, PURGE, & DELETE
 - These all point to deleting information that is already in the DB

CRUD VALIDATION

 - Permorming a CRUD analysis on your data model helps you check for scope
   and completeness
 - If you have a businesss rule that has no entity to CRUD against, then your
   data model may be incomplete
 - Similarly, if you have entities in your ERD that are not touched by any
   CRUD function (no business rule creates, retrieves, updates, or deletes from
   it), then you may not need that entity in your model

TERMINOLOGY

 - Consultant 
 - CRUD analysis
 - Functions

DD Section 5 Quiz
==============

If a relationship can NOT be moved between instances of the entities it 
connects, it is said to be:
 	Non-Transferable


Non-transferable relationships can only be mandatory, not optional. 
	False


Which of the following pairs of entities is most likely to be modeled as a 
1:1 relationship?
	PERSON and FINGERPRINT


If two entities have two relationships between them, these relationships can
be either _____________ or _____________ .
	Redundant or Required


Which of the following pairs of entities is most likely to be modeled as a M:M
relationship?
	TEACHER and SUBJECT AREA


A relationship on an ERD can have attributes. True or False?
	False

Many to many relationships between entities usually hide what?
	Another entity

When you resolve a M:M by creating an intersection entity, this new entity will
always inherit:
	A relationship to each entity from the original M:N

If an intersection entity is formed that contains no attributes of its own,
its uniqueness may be modeled by
	Barring the relationships to the original entities 	


TEST: DD DATABASE DESIGN MIDTERM EXAM
	SECTION 1

Software cannot operate without Hardware. True or False? 
	True

 
	SECTION 2

Many reasons exist for creating a conceptual model. Choose three appropriate 
reasons from the options below.
	- They accurately describe what a physical model will contaion
	- They capture current and future needs
	- They model functional and informational needs


Which of the following entities most likely contains valid attributes?
(Choose two)
	Entity:Pet, Attributes: Name, Birthday, Owner
	Entity:Home, Attributes: Number of Bedrooms, Owner, Address, Date Build 


An Entity Relationship model is independent of the hardware or software used
for implementation. True or False?
	True


Which of the following statements are true about ERD's? (Choose Two)
	- A piece of information should only be found in one place on a ERD
	- You should not model derivable data


Which of the following can be found in an ERD? (Choose Two)
	- Attributes
	- Entities


Which of the following are true about Cardinality? (Choose two) 
	- Cardinality tells "how many"
	- Cardinality specifies only sigularity or plurality, but not a
	  specific plural number


A business rule such as "All accounts must be paid in full within 10 days
of billing" is best enforced by: 
	- Creating additional programming code to identify and report
	  accounts past due


Business rules are important to data modelers because: 
	- They capture all ofthe needs, processes, and required functionality
	  of the business


A subtype can have a relationship not shared by the supertype. True or False?
	- True

A non-transferable relationship means the relationship is manatory at both
sides. True or False?
	- False

Non-transferable relationships can only be mandatory, not optional.
True or False? 
	- False


What uncommon relationship is described by the statements: "Each DNA SAMPLE
may be taken from one and only one PERSON and each PERSON may provide one and
only one DNA SAMPLE"
	- One to Many Mandatory


# Section 6 - UIDs and Normalization


## DD 6-1: Artificial, Composite and Secondary UIDs

* It is the value or combination of values that enables the user to find that
  one unique item among all the rest

* Simple UID = single attribute
* Composite UID = combination of attributes

* Artifical UIDs = are those that don't occur in the natural worl but are
  created for purposes of identification in a system. For example ID

* UIDs can be both artifical and composite

* Sometimes the UID is a combination of an attribute and a relationship

* As we've seen before, the resolution of a M:M relatioship often results in 
  barred relationships from the intersection entity to the original ones

* Sometimes two or mode possible UIDs exists
* Primary UID = only one of the candidate UIDs
* Secondary UIDs = the other candidates

* A primary key allows you to access a specific record in a DB

### TERMINOLOGY

* Artifical UID
* Candidate UID
* Composite UID
* Primary UID
* Secondary UID
* Simple UID
* UID


## DD 6-2: Normalization and First Normal Form

* Redundancy causes unnecessary problem in a DB
* Normalization is a process that is used to eliminate these kinds of
  problems
* Store information in one place and in the best possible place

### First Normal Form (1NF)

* First Normal Form requires that no multi-valued attributes exist
* If an attribute is multi-valued, create an additional entity and relate it to
  the original entity with a 1:M relationship

### TERMINOLOGY

* First Normal Form (1NF)
* Normalization
* Redundancy

## DD 6-3: Second Normal Form

* Second Normal Form (2NF) requires that any non-UID attribute be dependent
  on (be a proprty of, or a characteristic of) the entire UID

### TERMINOLOGY

* Second Normal Form (2NF)

### QUIZ

* When is an entity in 2nd Normal Form?
	* When all non-UID attributes are dependet upon the entire UID.


## DD 6-4: Third Normal Form

* The rule of Third Normal Form (3NF) states that no non-UID attribute can be
  dependent on another non-UID attribute

* Third Normal Form prohibits transitive dependencies

* A transitive dependency exists when any attribute in an entity is dependent
  on any other non-UID attribute in that entity

### TERMINOLOGY

* Third Normal Form (3NF)
* Transitive dependency


# Test: DD Section 6 Quiz

* Any Non-UID attribute must be dependent upon the entire UID.
	* True


# Section 7 - Arcs, hierarchies, and Recursive Modeling


## DD 7-1: Arcs

* Arcs in data modeling help designers clarify an exclusive OR accross
  relationships

### Constraint

* Every business has restriction on which attribute values and which 
  relationships are allowed

* These restriction are called constraints

### Exclusive OR Relationship

* An Exclusive OR relationship is a relationship between one entity and two
  (or more) other entities where only one of the relationships can exist at a
  time

### Arcs

* An arcs always belongs to one entity 
* Arcs can include more than two relationships
* Not all relationships of an entity need to be included in an arc
* An entity may have several arcs
* An arc should always consist of relationships of the same optionality
* All relationships in an arc must be mandatory or all must be optional
* Relationships in an arc may be of different cardinality, althought this is
  rare
* Arcs and Super/subtypes both model mutual exclusiveness

### TERMINOLOGY

* Arc
* Constraint
* Exclusive OR relatinship
* Mutually exclusive ralationship

### Quiz

* Arc model an Exclusive OR constraint.
	* True

## DD 7-2: Hierarachies and Recursive Relationships

### Hierarchical

* Hierarchical structures are more explicit and are easier for most people to
  undestantd because they are very similar to an organization chart
* Each entitty can have its own mandatory attributes and relationships, if the
  business requires this (instead of all optional attributes and relationships,
  as you would have in a recursive)
* In this way. your data model truly reflects the bussiness rules

### Recursive

* Recursive relationships tend to be simpler becouse you are using onle one
  entity
* Your diagram will be less "busy"
* However, they are less specific - you cannot have mandatory attributes or
  relationships unless they are mandatory in all instances of the entity

### Drawing Convention

* The ERD convention to show a recursive relationship is draw as a loop, also
  known as a "pig's ear".

### TERMINOLOGY

* Hierarchal relationship
* Recursive relationship


## Test: DD Section 7 Quiz

* A recursive relationship must be Mandatory at the both ends.
	* False

* All relationships participating in an arc must be mandatory
	* False

* Which of the following can be added to a relationship?
	* An arc can be assigned

* Which of the following would best be represented by an arc?
	* STUDENT (University, Technical College)

# Section 8 - Changes and Historical Modeling

## DD 8-1: Modeling Historical Data

* Changing data over time:

### TERMINOLOGY

* Audit trail
* Historical data

## DD 8-2: Modeling Change : Time

* Time plays a role in many business models

### Conditional Non-transferability

* Non-transferability: a SHIFT ASSIGNMENT cannot be changed to another BOOTH (or
  to another VOLUNTEER)
* Nontransferable relationships are represented by a diamond in the ERD

### TERMINOLOGY

* Conditional non-transferability
* Non-transferability
* Time-related constraint

## DD 8-3: Modeling Change : Price

* Changes in price are often an important consideration when modelin business
  requirements
* We've seen that prices change over time
* Other types of information can also change, for different business reasons

### Journaling

* Whenever a systemm allows a user to modify or remove particular information,
  the question should be asked, "Do the old values need to be kept on record?"
* This is called "logging" or "journaling"
* A journal usually consists of both the modified value and the information
  about who did the modification and when it was done

### TERMINOLOGY

* Appreciation
* Depreciation
* Journaling and/or logging

## DD 8-4: Drawing Conventions for Readability

* The bigger and more complicated an ERD gets, the more challenging it becomes
  to lay out the pieces in a clear and readable format

* There are two drawing conventions that are widely in use:
	* one that places high volume entities towards the top left of the page,
 	  and one that places high volume entities towards the bottom right of
 	  the page

### Large ERD Drawing Conventions

* High volume entities are often the "central" or more important entities in a
  ERD

* They will have the highest number of relationships to other entities, and most
  of the business functions will affect the data stored in these entitites

* When high volume entities are on the upper left portion of the ERD, the crows
  feet will tend to point south and east

* When high volume entities are on the lower right portion of the ERD, the crows
  feet will tend to point north and west

### Clarity is Key

* Use conventions sensibly
* The major goal of creating the diagram is to give a representation of the
  model that can be used for communication purpose
* This means that you must never let a convention interfere with readability and
  clarity
* Often you will have a mix of conventions, depending on the amount of space you
  have and your own preference
* Clarity and readability are the main criteria

* For clarity and readability in an ERD:
	* Avoid crossing relationship lines
	* Avoid entities that overlap
	* Avoid relationship lines that cross entities
	* Use plenty of "white space"
	* Split larger ERDs into smaller sub-diagrams if required

### Use Sub-Diagrams

* When you have a very large diagram, it may also help to break it up into
  smaller diagrams of functionally related entities

* You could use the smaller sub-diagrams when presenting to different groups
  within the customer's company
* It is still important to have a big diagram that shows the whole picture (even
  if it has to be printed on a plotter or taped together from smaller peices of
  paper)
* They may be relationships between entities in different sub-models, and these
  must be represented somewhere

### TERMINOLOGY

* High volume entity
* White space


# Test: DD Section 8 Quiz

* Which of the following scenarios should be modeled so that historical data is
  kept? (Choose two)
  	* STUDENT and GRADE
	* LIBRARY and BOOK

* Historical data should always be kept. True or False?
	* False

* Which of the following would be a logical constraint when modeling time for a
  country entity?
	* Countries may change their names and/or borders over a pariod of time.

* When a relationship may or may not be transferable, depending on time, this is
  know as a/an:
	* Conditional Non-transferable Relationship

 
# Section 9 - Mapping

## DD 9-1: Introduction to Relational Database Concepts

* The conceptual data model will be transformed into a relation database design.
* This means that our entities, attributes, realationships and unique
  identifiers will be translated into objects in a relational database

* A relational database is a database that is seen by the user as a collection
  of two-dimensional tables, each containing rows and columns

### Language to Access Data

* Structured query language (SQL) allows us to access data in relational
  databases in an efficient way
* Instead of manualy searching through each row to find the record for employee
  number 200, we use the following SQL statement:
```
SELECT last_name, department_id
FROM employees
WHERE employee_id = 200;
```

### Primary key

* A primary key (PK) is a column or set of columns that uniquely identifies each
  row on a table
* Each table should have a primary key, and a primery key must be unique
* No part of the primary key can be null
* Each column, or combination of columns, is called a "candidate" key becouse it
  could be selected for use as the primary key
* Select one candidate key to be the primary key for the table
* The other candidates become alternate keys (or unique keys)

### Foreign Key

* A foreign key (FK) is a column, or combination of columns, in one table that
  contains values that match the primary key value in another table.
* If a primary key is composed of one or more foreign keys, the FK value cannot
  be NULL

* Column integrity

### Summary od Data-Integrity Rules

* Data-integrity rules (also know as constraint) define the relationally correct
  state for a DB

* Data-integrity rules ensure that users can perform only those operations that
  leave the DB in a correct, consistent state

### TERMINOLOGY

* Candidate key
* Column
* Foreign key
* Primary key
* Relational database
* Row
* Unique key


## DD 9-2: Basic Mapping: The Transformation Process

* A table is simple structure in which data is organized and stored
* Each column is used to store a specific type of value, such as employee
  number, last name, and first name
* The foreign key column refers to a column in another table

### Transforming Conceptual to Physical

* The conceptual model (ER diagram) is transformed into a physical model
* The physical implementation will be a relational database

### Terminology Mapping

* Changing from analysis (conceptual model) to implementation (physical model)
  also means changing terminology:
	* An entity becomes a table
	* An instance becomes a row
	* An attribute becomes a column
	* A primary unique identifier becomes a primary key 
	* A secondary unique identifier becomes a unique key
	* A relationship is transformed into a foreign-key column and a foreign
	  key constraint

### Table Diagram Notations

* The first row of the table diagram contains the table name and the short name
* The Key Type column should contain values of "pk" for the primary key , "uk"
  for the unique key, and "fk" for the foreign-key column

### Table Short Names

* For entity names of more than one wprd, take the:
	* First character of the first word
	* First character of the second word
	* Last character of the last word
* Example: JOB ASSIGNMENT gets a short name of JAT

* For entity names of one word but more than one syllable
	* First character of the first syllable
	* First character of the second syllable
	* Last character of the last syllable
* Example:
	* EMPLOYEE gets a short name of EPE and CLIENT gets a short name of CET

* A complete list naming restrictions can be found on otn.oracle.com

### TERMINOLOGY

* Map
* Reserved word
* Transform

## DD 9-3: Relationship Mapping

* A relationship creates one or more foreign-key columns in the table on the
  many side of the relationship
* We use the short name of the table to name the foreign-key column
* EMPLOYEES table, dpt_id is relationship with DEPARTMENT 

### Mapping of Nontransferable Relationships

* A nontransferable relationship in the conceptual model means that the
  foreign-key column in the DB table cannot be updated

* The foreign-key constraint by itself cannot enforce this in the DB

### TERMINOLOGY

* Cascade barred relationship
* Intersection entity
* Nontransferable relationship

## DD 9-4: Subtype Mapping

### Supertype Implementation: Single Table

* This choice produces a single table for the implementation of the supertype
  entity and its subtypes
* This is also called "single-table (or one-table) implementation"
* Rules: 
	* Tables: Only one table is createdm regardless of the number of
	  subtypes
	* Columns: The single table gets one column for each attribute of the
	  supertype, along with the original optionality of the attribute

### Supertype Implementation: Single Table

* Rules:
	* Identifiers: Unique identifiers transform into primary and unique keys
	* Relationships: Relationships at the supertype level transform as
	  usual, relationships at the subtype level are implement as optional
	  foreign-key columns
	* Integrity constraint: A check constraint is needed to ensure that for
	  each particular subtype, all columns that come from mandatory
	  attributes are not null

### Subtype Implementation: Two Table

* This is also called "two-table implementation"
* You create a table for each ofthe subtypes
* So, in reality, you could have more than two tables, if you had more than two
  subtypes

* Rules:
	* Tables: One table per first-level subtype
	* Columns: Each table get one column for each attribute of the supertype
	  along with its original optionality
	* Each table also gets one column for each attribute belonging to the
	  subtype along with its original optionality

### When to Consider Subtypes Implementation

* Subtype implementation may be appropriate when:
	* Subtypes have little in common, there are few attributes at the
	  supertype level and several at the subtype level
	* Most of the relationships are at the subtype level
	* Business rules and functionality are quite different between subtypes

### Supertype and Subtype (Arc) Implementation

* This choice produces one table for every entity
* The supertype table has a foreign key for each subtype table
* These foreign keys represent exclusive relationships
* They are optional becouse only one of them can have a value for each row in
  the table

### TERMINOLOGY

* Arc implementation
* Subtype implementation
* Supertype implementation

### QUIZ

* An "Arc Implementation" can be done just like any other Relationship - you
 simply add the required Foreign Keys.
	* False

* When mapping supertypes, relationships at the supertype level transform as
 usual. Relationships at subtype level are implement as foreign keys, but the
 foreign key columns all become mandatory.
	* False


## Test: DD Section 9 Quiz

* The explanation below is an example of which constraint type? A primary key 
  must be unique, and no part of the primary key can be null.
	* Entity integrity

* Identify all of the correct statements that complete this sentence: A primary 
  key is: (Choose Three)
	* A set is columns that uniquely each row in a table
	* A set of columns and keys in a single table that uniquely identifies
	  each row in a single table
	* A single column that uniquely identifies each row in a table

* Two entities A and B have an optional (A) to Mandatory (B) One-to-One 
  relationship. When they are transformed, the Foreign Key(s) is placed on:
 	* The table B

* In a physical model, many to many relationships are resolved via a structure 
  called a(n): ________________
  	* Intersection Table

* It is possible to implement non-transferability via a simple Foreign Key 
  Relationship. True or False?
  	* False

* When translating an arc relationship to a physical design, you must turn the 
  arc relationships into foreign keys. What additional step must you take with 
  the created foreign keys to ensure the exclusivity principle of arc 
  relationships? (Assume that you are implementing an Exclusive Design) 
  (Choose Two)
  	* Make all relationships iptional
	* Create an additional check constraint to verify that one foreign key
	  is populated and the others are not 

*  The "Arc Implementation" is a synonym for what type of implementation?
	* Supertype and Subtype Implementation

* An "Arc Implementation" can be done just like any other Relationship - you 
  simply add the required Foreign Keys. True or False?
 	* False

* Identify all of the incorrect statements that complete this sentence: A 
  primary key is...(Choose three)
  	* A single column that unique identifies each column in a table
	* A set of columns in one table that uniquely identifies each 
	  row in another table.
	* Only one column that must be null

* When mapping supertypes, relationships at the supertype level transform as 
 usual. Relationships at the subtype level are implemented as foreign keys, but 
 the foreign key columns all become optional. True or False?
 	* True
