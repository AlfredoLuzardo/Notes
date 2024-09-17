- The visibility of private data in a parent class is still limited to that class
- A child can possess data it cannot access directly
- Create getter and setter methods in the parent class so the child can access the data

- The protected visibility modifier limits access to that data/method to:
	- That class itself, and
	- that class's child classes wherever they are, and
	- any class in the same package

- It is not a good idea to make instance variables protected 
- Trust your own code in your own class
- Do not allow any class - child or otherwise to have direct access 
- Make setters and getters protected as well

```java
// BAD:
class Animal
{
	protected double weightKg;
	Animal(final double weightKg)
	{
		this.weightKg = weightKg;
	}
}

// GOOD:
class Animal
{
	private double weightKg;
	Animal(final double weightKg)
	{
		this.weightKg = weightKg;
	}
	// Make protected getters and setters
}
```
