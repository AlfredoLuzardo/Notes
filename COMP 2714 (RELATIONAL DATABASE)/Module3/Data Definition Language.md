Statements to **define the data**
- These statements create (and change) the database schema

Basic SQL DDL Statements
- Table Definition
	- CREATE TABLE
	- DROP TABLE
	- ALTER TABLE

---
**Creating Table in SQL**

- CREATE TABLE statement creates a new relation, by specifying its name, attributes and constraints

- The key, entity, and referential integrity constraints are specified within the statement after the attributes have been declared.

- The domain constraint is specified for each attribute

- Data type of an attribute can be specified directly or by declaring a domain (CREATE DOMAIN)

---
- SYNTAX:

![[Pasted image 20241011134229.png]]
	- CREATE TABLE Movie
		 (movieID INTEGER,
		  title CHAR(20),
		  year INTEGER,
		  PRIMARY KEY (moveID));


![[Pasted image 20241011134326.png]]
	- CREATE TABLE StarsIn (
		starID INTEGER,
		movieID INTEGER,
		role CHAR(20),
		PRIMARY KEY (starID, movieID)),
		FOREIGN KEY (starID) REFERENCES MovieStar(starID),
		FOREIGN KEY (movieID) REFERENCES Movie(movieID));


![[Pasted image 20241011134705.png]]
	- CREATE TABLE Employee (
		ssn CHAR (NOT NULL),
		name VARCHAR(20) (NOT NULL),
		dob DATE,
		address VARCHAR(20),
		sex CHAR,
		salary DECIMAL,
		mgrSSN CHAR,
		dNum INTEGER (NOT NULL),
		PRIMARY KEY (ssn),
		FOREIGN KEY (mgrSSN) REFERENCES Employee (ssn),
		FOREIGN KEY (dNum) REFERENCES Department (dNumber));

**Creating a table with constraints**

![[Pasted image 20241011135829.png]]

- CREATE TABLE Employee (
		ssn CHAR (NOT NULL),
		name VARCHAR(20) (NOT NULL),
		dob DATE,
		address VARCHAR(20),
		sex CHAR,
		salary DECIMAL,
		mgrSSN CHAR,
		dNum INTEGER (NOT NULL),
		CONSTRAINT empPK PRIMARY KEY (ssn),
		CONSTRAINT empMgrFK FOREIGN KEY (mgrSSN) REFERENCES Employee (ssn),
		CONSTRAITN empDNumFK FOREIGN KEY (dNum) REFERENCES Department (dNumber));

**Semantic Constraints: Check**
	- CREATE TABLE Employee (
			ssn CHAR (NOT NULL),
			name VARCHAR(20) (NOT NULL),
			dob DATE,
			address VARCHAR(20),
			sex CHAR,
			salary DECIMAL,
			mgrSSN CHAR,
			dNum INTEGER (NOT NULL),
			PRIMARY KEY (ssn),
			FOREIGN KEY (mgrSSN) REFERENCES Employee (ssn),
			FOREIGN KEY (dNum) REFERENCES Department (dNumber)
			**CHECK (salary >= 10000 AND salary < 150000**);

**Enforcing Referential Integrity**

![[Pasted image 20241011142035.png]]

![[Pasted image 20241011145038.png]]

CREATE TABLE StarsIn (
	starID INTEGER,
	movieID INTEGER,
	role CHAR(20),
	PRIMARY KEY (starID, movieID),
	FOREIGN KEY (starID) REFERENCES MovieStar (starID)
	ON DELETE CASCADE
	ON UPDATE CASCADE,
	FOREIGN KEY (movieID) REFERENCES Movie (movieID)
	ON DELETE CASCADE
	ON UPDATE CASCADE)
);

Constraints that cannot be defined in one table using CHECK or based on referential integrity are defined as ASSERTIONs which are not associated with any table.

![[Pasted image 20241011145219.png]]

EXAMPLE: Every MovieStar needs to star in at least one movie

CREATE ASSERTION totalEmployment
CHECK
( NOT EXISTS (
	SELECT starID
	FROM movieStar
	WHERE starID NOT IN ( SELECT starID
						FROM StarsIn)));

----------------------------------
**ALTER TABLE**