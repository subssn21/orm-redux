orm-redux
=========

GIT project to accompany Talk proposal for PyOhio about ORMs and straight SQL in Python

Why ORMs

Object Mapping

Relationship Mapping

Pooling/connection management

DDL management

Where ORMs Shine

CRUD

Getting started on an app

Where ORMs fall down

Complex Joins

N + 1 problem

Custom Data types

Bulk insert/update operations

Performance

It can be very difficult to match a database query to the code that created it.

Conclusions

There is no "right" answer

You can't be afraid of SQL, it's often the best choice for somethings and sometimes the only choice.

You will often want to mix and match your ORM with plain SQL. some libraries are better than others for that.

Enum issues in ORMs
http://techspot.zzzeek.org/2011/01/14/the-enum-recipe/

Query to get the values of ENUM for an ENUM type
SELECT e.enumlabel
  FROM pg_enum e
  JOIN pg_type t ON e.enumtypid = t.oid
  WHERE t.typname = 'myenum'
  
  Get All Enums
  select * from pg_type where typtype = 'e';
