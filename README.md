orm-redux
=========

GIT project to accompany Talk proposal for PyOhio about ORMs and straight SQL in Python

Enum issues in ORMs
http://techspot.zzzeek.org/2011/01/14/the-enum-recipe/

Query to get the values of ENUM for an ENUM type
SELECT e.enumlabel
  FROM pg_enum e
  JOIN pg_type t ON e.enumtypid = t.oid
  WHERE t.typname = 'myenum'
