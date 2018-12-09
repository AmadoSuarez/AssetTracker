# VR AssetTracker - database design documentation

## Data System Overview:
  This overview contains a list of each table and their relationships with each other.

The AssetTracker data management system contains four Entity Components.  They are the COMPANY data which contains a unique company_id which is the Super key that will represent all data in the company tuple of the company along with company_name, the USERS data containing data of every user (administrators, freelancers, and customers); the attributes which combine themselves into creating the USERS entity are the composition key (Fname, Lname), username, email, password, create_time (registration time), a ForeignKey pertaining to the company_id and the primary key for Users, user_id. Next Entity is the MEMBERSHIPS Entity, which will represent the different memberships that USERS will be able to register for, the attributes of MEMBERSHIP are the different memberships offered and the foreign key of users, VRAssets and Company, and finally the VRAssets Entity, which will represent all Assets belonging to the company and respectful users. 


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
## First draft of Table Assets
![Image of Table_Assets](https://github.com/AmadoSuarez/AssetTracker/blob/database_joan/Table_assets.png)

### Table Asset
**Field/Attribute** | idVRAssets | Asset_name | Asset_size | Asset_quality
------------ | ------------- | ------------- | -------------
**Datatype** | INT | VAR CHAR (45) | VAR CHAR (45) | VAR CHAR (45) 
------------ | ------------- | ------------- | -------------
**Flagtype** | PK, NN, UQ | NN | N/D | N/D 

