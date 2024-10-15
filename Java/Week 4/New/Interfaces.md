
Java has three types involved in polymorphism:
- **Interfaces**
	- If you implement this interface, you **must** implement its abstract methods
- **Abstract Classes**
	- No objects can be created of this class, which is still very useful as a parent class containing all common traits for child class which extend this class
- **Concrete**
	- The kind of classes we have used so far: to create objects

![[Pasted image 20241003094913.png]]

**Interface**
- An interface is a collection of public static final data and abstract methods
	- (now it can also contain "default" concrete methods too)

**Abstract**
- Class that cannot have objects instantiated from it 
- It is an idea: put common methods and data there
- An abstract method has no body: it has only a method signature

- An **interface** is (in general) a set of **abstract methods** and **public static final data**
- An interface can also have default (concrete) methods
- A class can implement zero, one, or more interfaces
- That class must (a) implement all abstract methods and/or (b) be abstract itself

**Parent Classes**
- Any non-final class ("Parent class aka super class") can be extended by another class ("Child class aka sub class")
- The parents non-private data and methods are inherited by the child
- The child's constructor(s) must call one of its parents constructors with the proper parameters, by calling super() as its first instruction.

