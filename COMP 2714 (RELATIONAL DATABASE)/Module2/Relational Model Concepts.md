
**Relations**:
- Is the main construct for representing data in the relational model
- Is a set of records
- Is similar to a table with columns and rows
- Have specific properties, based on mathematical **set theory**

The term **table** is used interchangeably with **relation**
- Every relation is a table
- Not every table is a relation

**Relation Components**:
![[Pasted image 20240913144113.png]]

**Domain Types**:
- A **domain** D is a set of **atomic values**
- An atomic value is indivisible (as far as the relational data model is concerned)
- Each **domain** has a datatype or format:
	- Integers
	- Numbers and currency
	- Fixed or variable length character strings
	- Date, timestamp
	- Sub-range from a datatype
		- e.g., 1 <= grade <= 7
	- Enumerated data type
		- e.g. Gender in {‘Male’, ‘Female’, ‘Other’}
	- Australian Telephone Numbers
		- Format: the digits "61" followed by the digits 0-9
	- Car registration numbers
		- Format: 6 characters (either alpha or digits but no 'Q's allowed)

**Attributes**:
- Each attribute A is the name of a role played by some domain D in the relation named R
- The number of attributes in a relation R is called the **degree** of R
- Example: *salary* is an attribute name
![[Pasted image 20240920114321.png]]

**Domain/Attribute Restrictions**
- Same attribute name does not necessarily imply same domain


Domains for Department.ID and Employee.ID are different, even though attribute names are the same
  ![[Pasted image 20240920114643.png]]

- Different attribute name does not necessarily imply different domain

![[Pasted image 20240920114726.png]]

**Tuples**
- Each **tuple** t is an **ordered list** of n values:
	- t = <v<sub>1</sub>, v<sub>2</sub>, ..., v<sub>n</sub>>
- where each value , v<sub>¡</sub> (1 ≤ ¡  ≤ n) is an element of the corresponding domain of attribute A<sub>¡</sub> or a special value called "NULL"
- t is called an n-tuple
- Example: (1751, Paris Lane, 60,000, 2, NULL) is a 5-tuple

**Relation Schema and Instance**
- Relation Schema:
	- Denoted by R [A<sub>1</sub>, A<sub>2</sub>, A<sub>3</sub>, ..., A<sub>n</sub>], includes a relation name R and list of attributes A<sub>1</sub>, A<sub>2</sub>, ..., A<sub>n</sub>
	- Integer n is termed "degree of the relation"
	- A relation schema of degree 5
		- Employee [id, name, sex, salary, department]
	- ![[Pasted image 20240920120028.png]]

- Relation Instance:
	- A relation instance r of the relation schema R, denoted by r(R), is a set of n-tuples  r = {t<sub>1</sub>, t<sub>2</sub>, ..., t<sub>m</sub>}.
	- ![[Pasted image 20240920120046.png]]

**Ordering of Tuples**
- Relations are sets of tuples
- **Mathematically**, elements of a set have no implied order
- **Semantically**, when reasoning with relations, e.g. when formulating queries, order is irrelevant
- **Physically**, tuples reside on blocks of secondary stage, which have partial ordering, hence tuples have an ordering
- ![[Pasted image 20240920120437.png]]
**Ordering of values within a Tuple**
- n-tuple is an *ordered* list of n values
- **Syntactically**, all tuples in a relation have values in the same order
- **Semantically**, the order chosen is irrelevant, as long as the correspondence between the attributes and the values can be maintained
- ![[Pasted image 20240920120702.png]]
