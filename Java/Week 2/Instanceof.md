- Not used often
- It returns true if an object is of the specified class, or is some child (grandchild, etc.) of it.

```java
final Animal a3;

a3 = new Pitbull(50.0, "Rocky", true);

System.out.println(a3 instanceof Object); // true for all classes
System.out.println(a3 instanceof Animal); // true
System.out.println(a3 instanceof Dog); // true
System.out.println(a3 instanceof Pitbull); // true
System.out.println(a3 instanceof Dolphin); // false

```

**getClass()**

- The object class has methods available to absolutely all classes, since all classes (including arrays) automatically extend it 

- The object class has methods that may be used in place of the instanceof operator: getClass() and getName() and getSimpleName() (no package)

```java
package ca.bcit.comp2522.zoo;
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

		System.out.println(a1.getClass()); // class ca.bcit.comp2522.zoo.Animal
		System.out.println(a2.getClass().getName()); // ca.bcit.comp2522.zoo.Dog
		System.out.println(a2.getClass().getSimpleName()); // Pitbull
	}
}
```
