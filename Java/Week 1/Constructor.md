- Called automatically whenever an object is being created with the "new" keyword
- same name as class
- Guaranteed to either return an object of that class, or an exception
- Its job is to initialize an object

**Instance initializer blocks**
- Even before a constructor is executed, instance initializer blocks are executed for new objects
- These can be used when multiple constructors are re-using the same bunch of code
- In reality, used rarely

**Static initializer blocks**
- When a class is loaded into memory by the Java Virtual Machine, its static fields and methods are accessible
- a class is loaded into memory (loaded, linked, and initialized)
	- when an instance of the class is created
	- when a static field or method of the class is accessed
	- when Class.forName("classname") is called
	- when a subclass is instantiated or its static members are accessed
	- when a reflection is used to access or modify a class
- Static initializer blocks can be used to set up complex data or logic

**Validation methods**:
- Constructors main job is to set up objects with valid initial states
- non-final data also has setter methods that must also validate data
- to guarantee that proper validation methods are always called, create private static validation methods
- private static methods are not overridable which is important
- call these methods from the constructors and the mutators 
- all the validation methods need do is throw exceptions with bad data values

**Overloading**:
- A class can have multiple constructors as long as signatures differ
- Methods can also be overloaded this way

**Constructor chaining**:
- this() means the code is calling its own constructor
- if you have two or more constructors, avoid code duplication by having one that does most of the work, and the others call that one