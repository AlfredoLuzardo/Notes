**Database Integrity Constraints**
- **Integrity Constraints** are specified on the database schema
	- They must hold on every instance of that schema, as well as on transitions of the schema
- Integrity constraints enforced by DBMS include:
	- Domain constraints
	- Key constraints
	- Entity integrity constraints
	- Referential integrity constraints
	- Semantic integrity constraints

**Domain Constraints**
- A **domain** is a set of atomic values
- Each attribute in a relation will belong to some domain
- Assuming the domain of Employee.id is a 4 digit integer then:
![[Pasted image 20240920133644.png]]

**Uniqueness and Superkey**
- **Uniqueness Constraint**: All tuples in a relation must be distinct (i.e. no two tuples can have same values for all attributes)
![[Pasted image 20240920133948.png]]

- A **superkey** is a subset of attributes (SK) of a relation schema R, such that for any two tuples, t<sub>i</sub> and t<sub>j</sub> in a relation state r of R.
				t<sub>i</sub> [SK] ≠ t<sub>j</sub>[SK]
- Every relation has at least one superkey
	- Trivially, the set of all its attributes

**Key**
- K is a **key** in a relation schema R if
	- K is a superkey of R, and
	- K does not contain any extraneous attributes
		- That is, any subset of K is no longer a superkey of R

- A key is a minimal superkey
	- Smallest set of attributes that uniquely identify a tuple

![[Pasted image 20240920134712.png]]

- A schema may have more than one key
	- Each is called a **candidate key**
	- One is selected as the **primary key**, which would be underlined




**MIDTERM**
Question to come up with ERD
ERD to come up with a schema
**MIDTERM**