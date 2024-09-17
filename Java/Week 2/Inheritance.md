
**Inheritance**:
- Allows one class (subclass or child class) to inherit properties and methods from another class (superclass or parent class)
- This promotes code reuse and test reuse

![[Pasted image 20240913135457.png]] EXAMPLE HIERARCHY

**Benefits**:
- **Code and Test reusability**:
	- Allows the reuse of existing code by creating new classes based on existing ones
- **Extensibility:**
	- New features can be added to existing classes without modifying them (e.g. adding child classes and leaving the parent classes as is)
- **Maintainability**:
	- Centralized changes to the parent class propagate to all derived classes, simplifying updates and maintenance
- **Polymorphism**:
	- Enables objects of derived classes to be treated as instances of the parent class, enhancing flexibility and scalability
- **Modularity**:
	- Promotes modular design by separating common functionality into a base class and specialized behavior into derived classes