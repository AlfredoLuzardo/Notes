
- Nested class aka inner class ( unless its static)
- Outer class aka top-level class 

- Can be defined as:
	- private
	- protected
	- public
	- static

- Why?
	- If a particular class will only ever be needed by ONE other class, it is a candidate for being an inner (nested class).
	- The inner class has access to the data and methods of its containing (outer) class.

- Still, separating functionality into multiple classes - nested or not - makes it easier to read and maintain the code.

---

- Instance data can never be accessed from static contexts

- To outside classes, an instance of the nested class can be made by instantiating an instance first of the outer class, and then of the inner class.
	- However, if the nested class has private or protected visibility, then instances may not be instantiated from the outside. Also, if the inner class is static, it can exist on its own without first creating an outer-class object.

- Inner classes can directly access data and methods of the outer class, even if declared as private.

---

- Outer classes can indirectly access data and methods of the inner class (by an object of that inner class). However, children of the outer class cannot access those if private.