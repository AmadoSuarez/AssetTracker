# VR AssetTracker - database design documentation

## Data System Overview:
  This overview contains a list of each table and their relationships with each other.
  > Note to reader/learner:
  > * This documentation is not based on a final draft. 
  > Tables and the schema as a whole will change into something more complex by the end of the project.

The AssetTracker data management system contains four Entity Components.  They are the COMPANY data which contains a unique company_id which is the Super key that will represent all data in the company tuple of the company along with company_name, the USERS data containing data of every user (administrators, freelancers, and customers); the attributes which combine themselves into creating the USERS entity are the composition key (Fname, Lname), username, email, password, create_time (registration time), a ForeignKey pertaining to the company_id and the primary key for Users, user_id. Next Entity is the MEMBERSHIPS Entity, which will represent the different memberships that USERS will be able to register for, the attributes of MEMBERSHIP are the different memberships offered and the foreign key of users, VRAssets and Company, and finally the VRAssets Entity, which will represent all Assets belonging to the company and respectful users. 



## First draft of Table Assets - Figure 1.2
![Image of Table_Assets](https://github.com/AmadoSuarez/AssetTracker/blob/database_joan/Table_assets.png)

### Table Asset
---
| **Field/Attribute** | idVRAssets | Asset_name | Asset_size | Asset_quality |
| --------             | -------- |   -------- |   -------- |     -------- |
| **Datatype** |           INT | VAR CHAR (45) | VAR CHAR (45) | VAR CHAR (45) |
| **Flagtype** | PK, NN, UQ | NN |        N/D |            N/D |

*This table version was created only to have a clear understanding about:*
  > Field/Attributes,
  > Datatypes of Fields and 
  > Flagtype of Fields.
  
**Figure 1.2 Definition**

•	This is the database table for VR Assets. **Assets** is known as the *Entity* or *table name*.

•	**Fields** are the attributes pertaining to an Entity. Fields/Attributes are placed on the zero row of a table and the values pertaining to such field/attribute are below them forming a column.

•	Column 1 or idVRAssets is (*as defined on Figure 1.1*) the column reserved for the ID field. The id field will always (or more likely) be referred as a *primary key*, or *unique key* of a table and *not null* (**NN**), or sometimes all of the above. as noted on the *Flagtype* row. ***idVRAssets*** is defined to be of Int type, know why? Yes, inputs can only be of type integer.

•	Column 2 or Asset_name, is the column reserved for the particular name of an Asset but, what about other assets with the same name? Ahh great question! 
* The answer is that none of the tablets or the schema itself is a final draft yet.
* These tables and definitions are only to have a broad understanding of what a final version of the schema will be.
* In conclusion, this is some sort of documentation to make path into the understanding of how databases work as explained briefly in the introduction of this documentation.


