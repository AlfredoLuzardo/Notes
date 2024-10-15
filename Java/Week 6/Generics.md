- Allows for parameterized types in classes, interfaces, and methods, providing type safety.
- Prevents runtime errors caused by incorrect data types.

In this example, Box`<T>` class can store any type, making it flexible:
```java
public class Box<T> 
{
	private T t;
	
	public void set(T t) 
	{
		this.t = t;
	}

	public T get()
	{
		return t;
	}
}
```

- The advantage of using generics in the Box`<T>` class is that it allows you to create a single class that can operate on objects of different types while maintaining type safety.

- Without generics, you'd either have to:
	- create separate classes for each type
	- or use a non-type-safe approach (like using Object), which would introduce the risk of runtime errors due to type mismatches.

WITHOUT GENERICS:
```java
public class BoxWithoutGenerics
{
	private Object t;
	
	public void set(Object t)
	{
		this.t = t;
	}

	public Object get()
	{
		return t;
	}
}

public class Main
{
	public static void main(final String[] args)
	{
		BoxWithoutGenerics box;
		box = new BoxWithoutGenerics;
		
		box.set("Hello"); // Storing a String
		String s = (String) box.get(); // Explicit casting is needed

		box.set(123); // Storing an integer
		Integer i = (Integer) box.get(); // Explicit casting again
	}
}
```
- Problems:
	- Explicit Casting:
		- You need to cast the result of get() to the expected type, which increases the risk of runtime ClassCastException errors if you mistakenly cast to the wrong type.
	- Lack of Type Safety:
		- There's no compile-time checking to ensure the type you're setting matches the type you're getting. For example, you might mistakenly store an Integer and attempt to retrieve it as a String, which would cause a runtime error.

WITH GENERICS:
```java
public class Main 
{
	public static void main(final String[] args)
	{
		Box<String> stringBox;
		stringBox = new Box<>();
		
		stringBox.set("Hello"); // Store a String
		String s = stringBox.get(); // No casting needed

		Box<Integer> integerBox;
		integerBox = new Box<>();

		integerBox.set(123); // Store an Integer
		Integer i = integerBox.get(); // No casting needed
	}
}
```

- Advantages of Generics:
	- No Casting Required:
		- With generics, the Box`<String>` knows that it must store and return String objects, and Box`<Integer>` knows that it must handle Integer objects. This eliminates the need for explicit casting when retrieving values.
	- Type Safety:
		- Generics provide compile-time type checking. If you try to store a String in a Box`<Integer>`, for example, the compiler will throw an error, preventing you from making that mistake.
	- Reusability:
		- You can use the same Box`<T>` class for any type (String, Integer, CustomObject, etc.), reducing code duplication and making your class more versatile.

---

Generic Methods
- Introduce their own type parameters, independent of the class type parameters.
	- This allows for flexibility when performing actions that don't depend on the class's generic type.
- Here the generic method works with any type that implements comparable:

```java
public class Utility
{
	public static <T extends Comparable> T getMax(T a, T b)
	{
		return a.compareTo(b) > 0 ? a : b;
	}
}
```

---

Bounded Types in Generics
- You can use bounds to restrict generic types with the extends or super keyword. This ensures that only certain specific types can be passed while still allowing flexibility.
e.g.
```java
public <T extends Number> void addNumbers(T a, T b)
{
	System.out.println(a.doubleValue() + b.doubleValue());
}
```
