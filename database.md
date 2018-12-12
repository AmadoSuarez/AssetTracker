# VR AssetTracker - database design documentation

## Data System Overview:
  This overview contains a list of each table and their relationships with each other.
  > Note to reader/learner:
  > * This documentation is not based on a final draft. 
  > Tables and the schema as a whole will change into something more complex by the end of the project.

The AssetTracker data management system contains four Entity Components.  They are the COMPANY data which contains a unique company_id which is the Super key that will represent all data in the company tuple of the company along with company_name, the USERS data containing data of every user (administrators, freelancers, and customers); the attributes which combine themselves into creating the USERS entity are the composition key (Fname, Lname), username, email, password, create_time (registration time), a ForeignKey pertaining to the company_id and the primary key for Users, user_id. Next Entity is the MEMBERSHIPS Entity, which will represent the different memberships that USERS will be able to register for, the attributes of MEMBERSHIP are the different memberships offered and the foreign key of users, VRAssets and Company, and finally the VRAssets Entity, which will represent all Assets belonging to the company and respectful users. 



