
- Class
- Interface
- Record
- Enum
- Annotation

**Class**:
- File that describes the data and behaviors of a general category
- The data are known as instance variables; fields, attributes, properties
- Behaviors are known as methods; functions, procedures
- Function called constructor, which is called automatically when instance of a class is being created
- CamelCase, starting with an uppercase first letter

**Object**:
- An instance of a class
- Keyword "new" is a way to make an object of a class

**Variables and Datatypes**:
- Variables must be explicitly declared with their datatype
- Two Categories:
	- Primitive: Int, double, char, etc.
		- Are simple, only hold one value
	- Reference Types: String, array, System, BankAccount, etc.
		- Are complex, hold the memory address of an object

**Default Types**:
- When java encounters a whole num, it is treated as int
- When java encounters a decimal, it is treated as double
- When java encounters true or false, treated as boolean
- When java encounters a single Unicode character in single quotes, it is treated as char
- When java encounters Unicode characters in double quotes, treated as String
- An array uses [square brackets]; it stores a fixed number of values of a single type
- int: 0
- double: 0.0
- boolean: false
- char: '\\u0000' (Unicode null character)
- String: null
- array: null

**NULL**
- A String is reference type
- Any reference type can be null, which means "there is no object"
- Strings have a variety of useful methods
- Be careful when using String methods, null has no methods
- null is not the same as ""
	- null means no string
	- "" is a string with no characters
		- but still is located at a memory address
		- has length() of 0
		- and still has string methods available
- if (s != null && !s.isEmpty())  GOOD CHECK, wont crash if s is null
- if (!s.isEmpty() && s != null) BAD CHECK, crashes if s is null