
**Instance Variables**
- Instance variables must be private, so other classes cannot directly alter their values
- Most instance variables should also be final; if you don't expect or want it to change, don't allow it
- if a variable belongs to a class, make it static
- Use the principle of least privilege:
	- Give the smallest possible access to your data (and methods, classes, etc...)

**Units and Naming**
- Variables must have very clear names
- Always put units in the name

	Bad:
		weight    date    name
	Good:
		weightKg    dateBorn    firstName

**Conventions: Final**
- Final means a variable cannot change its value after its been set once
- All arguments to all constructors and methods must be final
- Declare variables in one line, and initialize them in a separate line

**Static:**
- Variables can be static
- Methods can be static
- Nested classes can be static

- Static means "belongs to the class itself", not to objects
- Static means there is one single value per class (Not one per object)
- No objects are even required in order to access static data or methods 
- Static data can and do change

- Static methods cannot directly access non-static (instance) fields
	- Throws a compile error

**Symbolic Constants**
- Data that is both static and final are "symbolic constants"
- Symbolic constants use UPPERCASE_WITH_UNDERSCORE
- Use these often
- Never put numbers in your code
- Your work will not be marked until all "magic numbers" are gone