---
sidebar_label: 'Chapter 1 Before the Advent of Database Systems'
sidebar_position: 4
---

# Chapter 1 Before the Advent of Database Systems

The way in which computers manage data has come a long way over the last few decades. Today’s users take
    for granted the many benefits found in a database system. However, it wasn’t that long ago that
    computers relied on a much less elegant and costly approach to data management called the file-based
    system.

## File-based System

One way to keep information on a computer is to store it in permanent files. A company system has a
    number of application programs; each of them is designed to manipulate data files. These
    application programs have been written at the request of the users in the organization. New
    applications are added to the system as the need arises. The system just described is called the
    *file-based system*.


Consider a traditional banking system that uses the file-based system to manage the organization’s
    data shown in Figure 1.1. As we can see, there are different departments in the bank. Each has
    its own applications that manage and manipulate different data files. For banking systems, the
    programs may be used to debit or credit an account, find the balance of an account, add a new
    mortgage loan and generate monthly statements.

![Diagram with three coloured drawings: one of a woman and two men sitting and talking; the second shows a man shaking hands with a woman, both are standing and holding briefcases; the third is of a woman sitting. There are also drawings of labelled files, such as Employees, Checking Accounts and Mortgage Loans.](http://opentextbc.ca/dbdesign01/wp-content/uploads/sites/11/2013/12/FileBased-300x1701.jpg)

*Figure 1.1. Example of a file-based system used by banks to manage data.*

### Disadvantages of the file-based approach

Using the file-based system to keep organizational information has a number of disadvantages. Listed
    below are five examples.

#### Data redundancy

Often, within an organization, files and applications are created by different programmers from various
    departments over long periods of time. This can lead to *data redundancy*, a situation that
    occurs in a database when a field needs to be updated in more than one table. This practice can
    lead to several problems such as:

* Inconsistency in data format
* The same information being kept in several different places (files)
* *Data inconsistency*, a situation where various copies of the same data are
    conflicting, wastes storage space and duplicates effort

#### Data isolation

*Data isolation* is a property that determines when and how
        changes made by one operation become visible to other concurrent users and systems. This
    issue occurs in a concurrency situation. This is a problem because:

* It is difficult for new applications to retrieve the appropriate data, which
    might be stored in various files.

#### Integrity problems

Problems with *data integrity* is another disadvantage
    of using a file-based system. It refers to the maintenance and assurance that the data in a database are
    correct and consistent.Factors to consider when addressing this issue are:

* Data values must satisfy certain consistency constraints that are specified in
    the application programs.
* It is difficult to make changes to the application programs in order to enforce 
    new constraints.

#### Security problems

Security can be a problem with a file-based approach because:

* There are constraints regarding accessing privileges.
* Application requirements are added to the system in an ad-hoc manner so 
    it is difficult to enforce constraints.

#### Concurrency access

*Concurrency* is the ability of the database to allow multiple users access to the same record
    without adversely affecting transaction processing. A file-based system must manage, or prevent,
    concurrency by the application programs. Typically, in a file-based system, when an application opens a
    file, that file is locked. This means that no one else has access to the file at the same time.

In database systems, concurrency is managed thus allowing multiple users access to the same record. This
    is an important difference between database and file-based systems.

## Database Approach

The difficulties that arise from using the file-based system have prompted the development of a new
    approach in managing large amounts of organizational information called the *database approach*.

Databases and database technology play an important role in most areas where computers are used,
    including business, education and medicine. To understand the fundamentals of database systems, we will
    start by introducing some basic concepts in this area.

### Role of databases in business

Everybody uses a database in some way, even if it is just to store information about their friends
    and family. That data might be written down or stored in a computer by using a word-processing program
    or it could be saved in a spreadsheet. However, the best way to store data is by using *database management software*. This is a powerful software tool that allows you to store, manipulate
    and retrieve data in a variety of different ways.

Most companies keep track of customer information by storing it in a database. This data may
    include customers, employees, products, orders or anything else that assists the business with
    its operations.

### The meaning of data

Data are factual information such as measurements or statistics about objects and concepts. We use data
    for discussions or as part of a calculation. Data can be a person, a place, an event, an action or any
    one of a number of things. A single fact is an element of data, or a *data element*.

If data are information and information is what we are in the business of working with, you can start to
    see where you might be storing it. Data can be stored in:


* Filing cabinets
* Spreadsheets
* Folders
* Ledgers
* Lists
* Piles of papers on your desk


All of these items store information, and so too does a database. Because of the mechanical nature of
    databases, they have terrific power to manage and process the information they hold. This can make the
    information they house much more useful for your work.

With this understanding of data, we can start to see how a tool with the capacity to store a collection
    of data and organize it, conduct a rapid search, retrieve and process, might make a difference to how we
    can use data. This book and the chapters that follow are all about managing information.

## Key Terms

**concurrency**: the ability of the database to allow multiple users access to the
    same record without adversely affecting transaction processing

**data element**: a single fact or piece of information

**data inconsistency**: a situation where various copies of the same data are conflicting

**data isolation**: a property that
        determines when and how changes made by one operation become visible to other
        concurrent users and systems

**data integrity**: refers to the maintenance and assurance that the data in a
    database are correct and consistent

**data redundancy**: a situation that occurs in a database when a
    field needs to be updated in more than one table

**database approach**: allows the management of large amounts of organizational
    information

**database management software**: a powerful software tool that allows you to
    store, manipulate and retrieve data in a variety of ways

**file-based system**: an application program designed to manipulate data files 

## Exercises

1. Discuss each of the following terms:
    1. data
    1. field
    1. record
    1. file
1. What is data redundancy?
1. Discuss the disadvantages of file-based systems.
1. Explain the difference between data and information.
1. Use Figure 1.2 (below) to answer the following questions.
    1. In the table, how many records does the file contain?
    1. How many fields are there per record?
    1. What problem would you encounter if you wanted to produce a listing by city?
    1. How would you solve this problem by altering the file structure?

![A table listing project codes, names of project managers, phone numbers, addresses and bid prices.](http://opentextbc.ca/dbdesign01/wp-content/uploads/sites/11/2014/03/Ch1-Exercises-Figure1-1-e1409149351851.jpg)

*Figure 1.2. Table for exercise #5, by A. Watt.*

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
