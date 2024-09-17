- Refers to the ability to treat objects of different ("derived") classes through a common interface, typically the parent class, allowing methods to behave differently based on the objects actual type at runtime.

- Its about enabling flexibility were different objects can respond to the same method call in their own way.

- Substitution: (aka "the Liskov Substitution Principle")
	- Specifically refers to the idea that objects of a subclass should be able to replace objects of the parent class without affecting the correctness of the program

- **This means a child class object can be used wherever a parent class object is expected**


**Substitution**

```java
class Dolphin extends Animal
{
	private boolean inCaptivity;
	Dolphin(final double weightKg,
			final boolean inCaptivity)
		{
			super(weightKg);
			this.inCaptivity = inCaptivity;
		}

	protected boolean isInCaptivity()
	{
		return inCaptivity;
	}
}
```

```java
class Zoo
{
	public static void main(final String[] args)
	{
		final Animal a1;
		final Animal a2;
		final Animal a3;
		final Animal a4;

		a1 = new Animal(200.0);
		a2 = new Dog(30.0, "Rex");
		a3 = new Pitbull(50.0, "Rocky", true);
		a4 = new Dolphin(300.0, false);
	}
}
```

- The "static type" of all four animals is set at compile time.

- In this case, all of a1, a2, a3, and a4 have a static type of Animal.

- The "dynamic type" is set at runtime.

- In this case, the dynamic type of a1 is Animal, a2 is Dog, a3 is Pitbull, and a4 is Dolphin.

- A child can always be used in place of a parent in Java.