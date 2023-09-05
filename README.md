# Database Management

## System Design

### Softwaredevelopment Lifecycle
![alt text](https://github.com/aleksandraklofat/database_design_notes/blob/main/software%20development%20life%20cycle.png)

### Phase 1 - Requirements
What am I trying to build?
The scope

### Phase 2 - System Analysis

Taking requirements and analysing: time and what will be needed

### Phase 3 - System Architecture

We design system architecture

### Phase 4 - Building that software

There can be more phases.


## Model / modeling a database / Architecture

Model is a design to visualise, what we are going to build

Entity relationship diagram - we use it to create a model
What are we storing and how ? - Diagram


## Types of Databases
1. Regular 
2. Template


# Notes about Database Design
Notes about data base design and structure 

Before you implement a data base. You need to design it. 
You cannot start from CREATE table in postgres. 

# Phase 3: System Design

You take what stakeholders want to accomplish and form as tructure around it and you communicate this structure.

Different techniques to design databases. 

Question: What does the business needs?
Design that encompasses all requirements. 

Different techniques to desgin a database.

## 1. Top-down Design
Optimal choice when creating everything from scratch

1. current mission, current situation
2. requirements
3. how do we model database? 

Goal: create database model that is based on the requirements

this is interative. you design it iteratively. 
you have to have deep understanding of the business and how it function. 

### ER-Modeling / ERD (entity-relationship modeling)

1. Determine entities in the system
Entity: 
person/place/thing + singular name + has identifier + contain more than one instance of data

Model database as a chart

2. Atributes 
- must be property of entity
- can hold only single value (atomic)
- keys
- single/mutiple

## 2. Bottom-up Desgin
- there is a system/database
- for existing databases
