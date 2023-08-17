---
sidebar_label: 'Chapter 6 Classification of Database Management Systems'
sidebar_position: 9
---

# Chapter 6 Classification of Database Management Systems

Database management systems can be classified based on several 
criteria, such as the data model, user
    numbers and database distribution, all described below.

## Classification Based on Data Model

The most popular data model in use today is the relational 
data model. Well-known DBMSs like Oracle, MS
    SQL Server, DB2 and MySQL support this model. Other 
    traditional models, such as hierarchical data models
    and network data models, are still used in industry 
    mainly on mainframe platforms. However, they
    are not commonly used due to their complexity. These are all referred to as
    *traditional models* because they preceded the relational model.


In recent years, the newer *object-oriented data models* 
were introduced. This model is a
    database management system in which information is 
    represented in the form of objects as used in
    object-oriented programming. Object-oriented databases 
    are different from relational databases, which
    are table-oriented. Object-oriented database management 
    systems (OODBMS) combine database capabilities
    with object-oriented programming language capabilities.

The object-oriented models have not caught on as expected 
so are not in widespread use. Some
    examples of object-oriented DBMSs are O2, ObjectStore and Jasmine.

## Classification Based on User Numbers

A DBMS can be classification based on the number of 
users it supports. It can be a *single-user
        database system*, which supports one user 
        at a time, or a *multiuser database system*,
    which supports multiple users concurrently.

## Classification Based on Database Distribution

There are four main distribution systems for
            database systems and these, in turn, can be used to classify the DBMS.

### Centralized systems

With a *centralized database system*, the DBMS and 
database are stored at a single site
    that is used by several other systems too. This is illustrated in Figure 6.1.

![Diagram showing one large computer monitor and four small ones labelled Workstations or Terminals, with arrows between them. There is also a computer tower labelled Central Computer.](http://opentextbc.ca/dbdesign01/wp-content/uploads/sites/11/2013/12/Centralized-Systems-300x174.jpg)

*Figure 6.1. Example of a centralized database system.*

In the early 1980s, many Canadian libraries used the GEAC 8000 
to convert their manual card catalogues to
    machine-readable centralized catalogue systems. Each 
    book catalogue had a barcode field similar to those
    on supermarket products.

### Distributed database system

In a *distributed database system*, the actual database and the DBMS
        software are distributed from various sites that 
        are connected by a computer network, as shown in
        Figure 6.2.

![Diagram showing three circles, separately labelled Site 1-3, and each containing several computer monitors and a computer tower. A line connects each of these to a central oval marked Computer Network.](http://opentextbc.ca/dbdesign01/wp-content/uploads/sites/11/2013/12/Distributed-Systems-300x217.jpg)

*Figure 6.2. Example of a distributed database system.*

### Homogeneous distributed database systems

*Homogeneous distributed database systems* use the same 
DBMS software from multiple sites. Data
    exchange between these various sites can be handled 
    easily. For example, library information systems by
    the same vendor, such as Geac Computer Corporation, 
    use the same DBMS software which allows easy data
    exchange between the various Geac library sites.

### Heterogeneous distributed database systems

In a *heterogeneous distributed database system*, different sites
        might use different DBMS software, but there is additional 
        common software to support data exchange
        between these sites. For example, the various library 
        database systems use the same machine-readable
        cataloguing (MARC) format to support library record data exchange.

## Key Terms

**centralized database system**: the DBMS and database are
            stored at a single site that is used by several other systems too

**distributed database system**: the actual
                database and the DBMS software are distributed from various sites that are connected by a
                computer network

**heterogeneous distributed database system**: different
                sites might use different DBMS software, but there is
                additional common software to support data exchange between these sites
        
**homogeneous distributed database systems**: use the same DBMS software at
            multiple sites
        
**multiuser database system**: a database management system which supports
            multiple users concurrently
        
**object-oriented data model**: a database management system in which information is
            represented in the form of objects as used in object-oriented programming
        
**single-user database system**: a database management system which supports
            one user at a time

**traditional models**: data models that preceded the relational model

## Exercises

1. Provide three examples of the most popular relational databases used.
1. What is the difference between centralized and distributed database systems?
1. What is the difference between homogenous distributed database 
    systems and heterogeneous distributed database systems?

## Attribution

This chapter of *Database Design* (including its images,
    unless otherwise noted) is a derivative copy of [Database System
            Concepts](http://cnx.org/contents/b57b8760-6898-469d-a0f7-06e0537f6817@1)
             by Nguyen Kim Anh licensed under 
             [Creative Commons Attribution License 3.0 license](http://creativecommons.org/licenses/by/3.0/)

The following material was written by Adrienne Watt:

1. Key Terms
1. Exercises
