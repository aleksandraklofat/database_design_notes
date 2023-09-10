# Database Management

## System Design

### Softwaredevelopment Lifecycle
![alt text](https://github.com/aleksandraklofat/database_design_notes/blob/main/software%20development%20life%20cycle.png)

#### Phase 1 - Requirements
What am I trying to build?
The scope

#### Phase 2 - System Analysis

Taking requirements and analysing: time and what will be needed

#### Phase 3 - System Architecture

We design system architecture

#### Phase 4 - Building that software

There can be more phases.


## Model / modeling a database / Architecture

Model is a design to visualise, what we are going to build

Entity relationship diagram - we use it to create a model
What are we storing and how ? - Diagram


## Types of Databases
1. Regular 
2. Template


# Database Design
Notes about data base design and structure 

Before you implement a data base. You need to design it. 
You cannot start from CREATE table in postgres. 

## Phase 3: System Design

You take what stakeholders want to accomplish and form as tructure around it and you communicate this structure.

Different techniques to design databases. 

Question: What does the business needs?
Design that encompasses all requirements. 

Different techniques to desgin a database.

### 1. Top-down Design
Optimal choice when creating everything from scratch

1. current mission, current situation
2. requirements
3. how do we model database? 

Goal: create database model that is based on the requirements

this is interative. you design it iteratively. 
you have to have deep understanding of the business and how it function. 

#### ER-Modeling / ERD (entity-relationship modeling)

1. Determine entities in the system
Entity: 
person/place/thing + singular name + has identifier + contain more than one instance of data

Model database as a chart


2. Atributes 

In the context of databases, particularly relational databases, attributes refer to the properties or characteristics of an entity. They define the different types of data that can be stored about that entity.

for example, consider an entity "Person". The attributes for the "Person" might include:

    FirstName: The first name of the person.
    LastName: The last name of the person.
    DateOfBirth: The birth date of the person.
    EmailAddress: The email address of the person.
    PhoneNumber: The phone number of the person.

- must be property of entity
- can hold only single value (atomic)
- keys
- single/mutiple

Relation Schema - Table Schema: representation of data that is going into table </br>
Realtion Keys - inherently unique, identify the row and the relationship </br>
Primary Key - unique identifyier (we decide which one from relation keys will bekome primary key) </br>
Foreign Key - </br>
Compound Key - </br>
Composite Key - </br>
Surrogate Key - (actualy it is primary key - it represents unique row, id field) </br>

3. For every entity determine what things it will store/Atributes(?)

4. Drawing relationships between entities

Relationships: 1 to 1, 1 to many, many to many

Many to Many is very difficult to describe in relational databases. 
You need intermediate type: intermediate table

### 2. Bottom-Up Desgin

- there is a system/database
- for existing databases

#### 1. Data
Find data, identify Atributes (data that is required)

#### 2. Create entities out of data

#### Normalisation

Good description how normalisation works:
https://learn.microsoft.com/en-us/office/troubleshoot/access/database-normalization-description

creating data schema + entities
normalisation = design technique 

#### Functional Dependency
Functional dependency shows a relationship between attributes

If X → Y holds, then whenever two rows in a table have the same values for attributes in X, they will also have the same values for attributes in Y.


Here's a practical example:
Consider a relation (or table) with attributes StudentID, CourseID, and CourseName. If every CourseID is associated with a single CourseName, then we can say:

    CourseID functionally determines CourseName.
    This can be represented as: CourseID -> CourseName.

Based on the value of X, we can determine the value of Y. 

employee_nr → first_name
X → Y
Y is dependent on X (in order to identify its value)

#### Normalisation - Book (Link)
https://www.cs.uct.ac.za/mit_notes/database/htmls/chp09.html

## Normal Forms

### 0NF 

what kind of data is there ? /
data is unnormalized /
non atomic data 

### 1NF
- eliminated repeating data, repeating groups (repeating columns etc.)
- each atribute should contain a single value (Create a separate table for each set of related data)
- determine primary key

### 2NF
going to 2 you need to be in 1. You cannot skip the steps. 
- all non-key attributes are functionally dependent on the primary key

    "Create separate tables for sets of values that apply to multiple records.
    Relate these tables with a foreign key." (https://learn.microsoft.com/en-us/office/troubleshoot/access/database-normalization-description)


### 3NF 
Eliminate fields that don't depend on the key.

## Database Scalability