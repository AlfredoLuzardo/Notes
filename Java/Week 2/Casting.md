
- Convert between compatible types

- Put the new type in parentheses before the data itself

- We can use child specific classes this way

e.g.
```java
System.out.println((double)4); // Changes 4 to a double
// prints 4.0
```

```java
final Animal a3;
a3 = new Pitbull(50.0, "Rocky", true);

if(a3 instanceof Dog)
{
	final Dog d;
	d = (Dog)a3; // cast
	d.bark(); // treat as dog
}

if(a3 instanceof Dolphin)
{
	final Dolphin d;
	d = (Dolphin)a3;
	d.swim();
}
```

- You should often check the objects class before casting.
- Casting to an incompatible class will result in a **ClassCastException**:

```java
final Dolphin d1;
d1 = (Dolphin)a3; // compiles but...
d1.swim(); // CRASHES
```

