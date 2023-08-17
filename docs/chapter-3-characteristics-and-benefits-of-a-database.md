---
sidebar_label: 'Chapter 3 Characteristics and Benefits of a Database'
sidebar_position: 6
---

# Chapter 3 Characteristics and Benefits of a Database

Managing information means taking care of it so that it works for 
us and is useful for the tasks we
    perform. By using a DBMS, the information we collect and add 
    to its database is no longer subject to
    accidental disorganization. It becomes more accessible and 
    integrated with the rest of our work.
    Managing information using a database allows us to become 
    strategic users of the data we have.

We often need to access and re-sort data for various uses. These may include:

* Creating mailing lists
* Writing management reports
* Generating lists of selected news stories
* Identifying various client needs

The processing power of a database allows it to 
manipulate the data it houses, so it can:

* Sort
* Match
* Link
* Aggregate
* Skip fields
* Calculate
* Arrange

Because of the versatility of databases, we find them 
powering all sorts of projects. A database can be
    linked to:

* A website that is capturing registered users
* A client-tracking application for social service organizations
* A medical record system for a health care facility
* Your personal address book in your email client
* A collection of word-processed documents
* A system that issues airline reservations


## Characteristics and Benefits of a Database

There are a number of characteristics that distinguish 
the database approach from the file-based
    system or approach. This chapter describes the 
    benefits (and features) of the database system.

### Self-describing nature of a database system

A database system is referred to as *self-describing* 
because it not only contains the database
    itself, but also *metadata* which defines and 
    describes the data and relationships between
    tables in the database. This information is used 
    by the DBMS software or database users if needed. This
    separation of data and information about the data makes a database
    system totally different from the traditional 
    file-based system in which the data definition is part of
    the application programs.

### Insulation between program and data

In the file-based system, the structure of the data 
files is defined in the application programs so if a
    user wants to change the structure of a file, all 
    the programs that access that file might need to be
    changed as well.

On the other hand, in the database approach, the 
data structure is stored in the system catalogue and not
    in the programs. Therefore, one change is all that is needed to change the
        structure of a file. This insulation between the
    programs and data is also called program-data independence.

### Support for multiple views of data

A database supports multiple views of data.  
A *view* is a subset of the database, which is
    defined and dedicated for particular users of 
    the system. Multiple users in the system might have
    different views of the system. Each view might contain 
    only the data of interest to a user or group of
    users.

### Sharing of data and multiuser system

Current database systems are designed for multiple users. 
That is, they allow many users to access
    the same database at the same time. This access 
    is achieved through features called *concurrency
        control strategies*. These strategies ensure 
        that the data accessed are always correct and that
    data integrity is maintained.


The design of modern multiuser database systems is a great improvement from
        those in the past which restricted usage to one person at a time.

### Control of data redundancy

In the database approach, ideally, each data item 
is stored in only one place in the database. In some
    cases, data redundancy still exists to improve 
    system performance, but such redundancy is controlled by
    application programming and kept to minimum by introducing as
    little redudancy as possible when designing the database.

### Data sharing

The integration of all the data, for an organization, within a database
        system has many advantages. First, 
        it allows for data sharing among employees and others who have
        access to the system. Second, 
        it gives users the ability to generate more information from a given
        amount of data than would be possible without the integration.

### Enforcement of integrity constraints

Database management systems must provide the ability 
to define and enforce certain constraints to ensure
    that users enter valid information and maintain data
        integrity. A *database constraint* is a 
        restriction or rule that dictates what
    can be entered or edited in a table such as a 
    postal code using a certain format or adding a valid city
    in the City field.

There are many types of database constraints. 
*Data type*, for example, determines the sort of
    data permitted in a field, for example numbers only. 
    *Data uniqueness* such as the primary key
    ensures that no duplicates are entered. 
    Constraints can be simple (field based) or complex
    (programming).

### Restriction of unauthorized access

Not all users of a database system will have 
the same accessing privileges. For example, one user might
    have *read-only access* (i.e., the ability to 
    read a file but not make changes), while another
    might have *read and write privileges*, which is 
    the ability to both read and modify a file. For
    this reason, a database management system should 
    provide a security subsystem to create and control
    different types of user accounts and restrict unauthorized access.

### Data independence

Another advantage of a database management system is how it allows for data
        independence. In other words, the system 
        data descriptions or data describing data (metadata) are
        separated from the application programs. 
        This is possible because changes to the data structure
        are handled by the database management system 
        and are not embedded in the program
        itself.

### Transaction processing

A database management system must include concurrency control
        subsystems. This feature ensures that data 
        remains consistent and valid during transaction
        processing even if several users update the same information.

### Provision for multiple views of data

By its very nature, a DBMS permits many users to have access to its
        database either individually or simultaneously. 
        It is not important for users to be aware of how and
        where the data they access is stored.

### Backup and recovery facilities

Backup and recovery are methods that allow you to protect your data from
        loss.  The database system provides a separate process, 
        from that of a network backup, for
        backing up and recovering data. If a hard drive fails 
        and the database stored on the hard drive is
        not accessible, the only way to recover the database 
        is from a backup. If a computer system
        fails in the middle of a complex update process, the 
        recovery subsystem is responsible for making
        sure that the database is restored to its original state. 
        These are two more benefits of a database
        management system.

## Key Terms

**concurrency control strategies**: features of a database that allow several users
            access to the same data item at the same time

**data type**: determines the sort of data permitted in a field, for example
            numbers only

**data uniqueness**: ensures that no duplicates are entered

**database constraint**: a restriction that determines what is allowed to be entered
            or edited in a table

**metadata**: defines and describes the data and relationshipsbetween tables in
            the database

**read and write privileges:** the ability to both read and modify a file

**read-only** **access:** the ability to read a file but not make
            changes

**self-describing**: a database system is referred to as self-describing
            because it not only contains the database itself, but also metadatawhich defines and describes
            the data and relationships between tables in the database

**view**: a subset of the database


## Exercises

1. How is a DBMS distinguished from a file-based system?
1. What is data independence and why is it important?
1. What is the purpose of managing information?
1. Discuss the uses of databases in a business environment.
1. What is metadata?

## Attribution

This chapter of *Database Design* (including its images,
    unless otherwise noted) is a derivative copy of [Database System
            Concepts](http://cnx.org/contents/b57b8760-6898-469d-a0f7-06e0537f6817@1)
             by Nguyen Kim Anh licensed under 
             [Creative Commons Attribution License 3.0 license](http://creativecommons.org/licenses/by/3.0/)

The following material was written by Adrienne Watt:

1. Introduction
1. Key Terms
1. Exercises
