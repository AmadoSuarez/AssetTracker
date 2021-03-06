### Example table: Figure 1.1

  Users (Entity) 
  ---
  | U_id | U_position | U_name | other.id (FK) |
  | -------- | -------- | -------- | -------- |
  | 123456789   | freelancer   | “Joan Quintero”  |  222  | 


**Figure 1.1 Definition**

•	This is the database table for Users. Therefore, Users is known as the Entity.
•	Fields are the attributes pertaining to an Entity. Fields/Attributes are placed on the zero row of a table and the values pertaining to such field/attribute are below them forming a column.
•	Column 1 or Entity_id is the column reserved for the ID field. The id field will always (or more likely) be referred as a primary key, or unique key of a table. 
•	Column 2 or Entity_position in this table, is the column reserved for position of the user or job title.
•	Column 3 or Entity_name in this table, is the column reserved for name of user.
•	Lastly, Column 4 or ForeignKey.otherEntity_id is a unique column in the table (note: some tables do not need a Foreign Key attribute known as reference) and in this, FK vas a value of “222” which refers to the id of another table. (check below for Foreign Key definition)

**Definitions:**

**Primary Key:** A primary key, also called a unique key, is a value in a relational database that is unique for each record (or row).
**Row:** is an ordered set of known or unknown values with names.
**Foreign Key:** A foreign key is a column (or columns) that references a column (most often the primary key) of another table. 
 
---
