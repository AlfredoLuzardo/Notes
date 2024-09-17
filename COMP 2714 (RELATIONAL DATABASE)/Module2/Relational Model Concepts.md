
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