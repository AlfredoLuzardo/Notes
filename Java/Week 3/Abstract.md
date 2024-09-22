- ABSTRACT == JUST A CONCEPT; DOES NOT ACTUALLY EXIST
- NO OBJECTS CAN BE MADE

- Any class that we know so far, at any time, can be made abstract
- The opposite of an abstract class is a concrete class

- **An abstract class can contain**:
	- only abstract methods, **e.g.** *public abstract void foo();*
	- only concrete methods, **e.g.** *public void foo(){}*
	- a mix of abstract and concrete methods
	- no methods
	- instance variables, statics, constants
	- constructors 

EXAMPLES:
abstract Animal
abstract Dog
Chihuahua

abstract Database
abstract MySql
MySql5.6 for Windows

![[Pasted image 20240918120335.png]]

**Abstract Methods**
- An abstract method has no body at all
- "I won't tell you what to do, but my children *must*"

```java
public abstract void move(); // no curly braces {}
```
		OR
```java
public abstract void move(int c, String y); // no curly braces {}
```

**Abstract Classes**
1. If a class has one or more abstract methods, the class **MUST** be declared abstract

2. An abstract class cannot have objects made of it; it is just an *idea*

3. For a class to be concrete (i.e. not abstract; objects can be made of it), that class must implement (override) all parent (grandparent, etc...) methods which were abstract. In other words, if a parent has abstract methods, and its child doesn't override them, the child must be abstract.

