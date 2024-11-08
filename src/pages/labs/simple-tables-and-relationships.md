---
title: Simple Tables and Relationships
description: Simple Tables and Relationships
hide_table_of_contents: false
---

# Simple Tables and Relationships

## Re-implent the AppSheet Database in MariaDB/MySQL

Follow the in-class instructions to re-implement
the AppSheet database from the previous lab in MariaDB/MySQL.

Insert 5 sample records into the table.

## Course Table

Using phpMyAdmin create a new course table in
your nXXXXXXX_cps146_a2 database.

1. Select your nXXXXXXX_cps146_a2 database.
1. Name the new table "Course".
1. Set number of columns to 4.
1. Click on the "Go" button.
1. For the subject code column:
   1. For "Name", enter "SubjectCode".
   1. For "Type", choose "ENUM".
   1. Under "Length/Values", click the "Edit ENUM/SET values" link.
   1. Enter "CPS" and "DGL"; delete the two blanks; and click the "Go" button.
   1. For the "Index", choose "PRIMARY"; click the "Go" button.
1. For the course number column:
   1. For "Name", enter "CourseNumber".
   1. For "Type", choose "INT".
   1. For "Length/Values", enter "3".
   1. For the "Index", choose "PRIMARY"; click the "Go" button.
1. For the title column:
   1. For "Name", enter "Title".
   1. For "Type", choose "VARCHAR".
   1. For "Length/Values", enter "50".
1. For the credits column:
   1. For "Name", enter "Credits".
   1. For "Type", choose "INT".
   1. For "Length/Values", enter "1".
1. Click on the "Save" button at the far bottom right of the form.
1. Go to "Insert" tab.
1. Fill out some sample data in the "Value" column of the form and use
   the "Go" button to insert the new record.
1. Repeat until you have 5 records in the table.
1. Try adding a record with a duplicate SubjectCode/CourseNumber and
   convince yourself this does not work.

## Event Table

Create an "Event" table. You will need to record the building
which is one of "KMX", "DIS", "RAV", or "TYE". You will also
need the room number which is a 3 digit number. Each event
will also have a title and a starting and ending time.

Set a natural primary key that will at least prevent multiple
events being scheduled to start in the same room at the same
time. Don't worry about other overlapping for now.

Enter 5 sample records into your new table.

## Relationships

### In-class

Follow the in-class instructions to implement the following
tables and relationships.

High-level model:

```mermaid
%%{init: {'er': {'layoutDirection': 'LR'}}}%%
erDiagram
    FLIGHT }o--o{ PASSENGER : "books"
```

Implementation (table-level) model:

```mermaid
%%{init: {'er': {'layoutDirection': 'LR'}}}%%
erDiagram
    FLIGHT ||--o{ BOOKING : ""
    BOOKING }o--|| PASSENGER : ""
```

```mermaid
%%{init: {'er': {'layoutDirection': 'LR'}}}%%
erDiagram
    FLIGHT ||--o{ BOOKING : ""
    BOOKING }o--|| PASSENGER : ""
    FLIGHT {
        int ID PK
        varchar origin
        varchar destination
        time time
    }
    BOOKING {
        int flightID PK,FK
        int passengerID PK,FK
        varchar seat
    }
    PASSENGER {
        int ID PK
        varchar name
    }
```

### On Your Own

Create the tables and some sample data (at least 5 records in each
table) for a hair salon based on the
following high-level model.

```mermaid
%%{init: {'er': {'layoutDirection': 'LR'}}}%%
erDiagram
    CUSTOMER ||--o{ APPOINTMENT : "books"
```

Be sure to create the appropriate primary and foreign keys. Also,
be sure to add any additional attributes to the tables that
seem relevant.
