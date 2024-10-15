**Relational Query**
- **INSERT**: New tuples may be inserted 
- **DELETE**: Existing tuples may be deleted
- **UPDATE**: Values of attributes in existing tuples may be changed
- **SELECT**: Attributes of specific tuples, entire tuples, or even entire relations may be retrieved

**SQL**
- It is a relational query language
- Declarative language for users to specify what the result of the query should be, and the DBMS decides operations and order of execution
- Designed for *data definition*, *data manipulation*, and *data control*, powerful enough to retrieve any piece of data from the database.

Three types of SQL statements
- **Data Definition** Language (DDL)
	- Statements to define the database schema

- **Data Manipulation** language (DML)
	- Statements to manipulate the data

- **Data Control** language (DCL)
	- Statements to specify **transaction control**, **semantic integrity** (triggers and assertions), authorization and management of privileges.
	- Statements for specifying the **physical storage parameters** such as **file structures and access paths (indexes)**
	- Statements to specify the **role-based security controls**.