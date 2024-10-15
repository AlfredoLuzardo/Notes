
- An interface is a collection of public static final data and abstract methods
	- Now it can also contain default concrete methods
- A class can implement zero, one, or more interfaces
- That class must  (a) implement all abstract methods and/or (b) be abstract itself

![[Pasted image 20240925085646.png]]

```java
abstract class Animal implements Speakable, Moveable
{
	public int minDB()
	{
		return Speakable.super.min();
	}
	
	public int minSpeed()
	{
		return Moveable.super.min();
	}

	@Override
	public int min()
	{
		return 1000;
	}
}
```

```java 
class Cheetah extends Animal
{

	@Override
	public void speak()
	{
		System.out.println("Purrrr");
	}
	
	@Override
	public double getMaxSpdKmPerSec()
	{
		return 0.1;
	}
}
```

```java
class Dog extends Animal
{
	private final String name;

	Dog(String name)
	{
		this.name = name;
	}

	@Override
	public double getMaxSpdKmPerSec()
	{
		return 0.05;
	}
}
```

```java
interface Speakable
{
	void speak();

	
	default int min()
	{
		return -15;
	}
}
```

```java
interface Moveable
{
	int MAX_SPD_KM_PER_SEC = 300000;

	default double getMaxSpdKmPerSec()
	{
		return MAX_SPD_KM_PER_SEC;
	}

	/**
	 * @return speed
	 */
	default int min()
	{
		return 0;
	}
}
```

-----------------------------

// ON QUIZ
```java
public class Student 
		implements Comparable<Student>
{
	private final int yearBorn;
	private final String firstName;
	private final double gpa;

	Student(final int yearBorn, 
			final String firstName, 
			final double gpa)
	{
		this.yearBorn = yearBorn;
		this.firstName = firstName;
		this.gpa = gpa;
	}

	/**
	 * Longer first names are "bigger" students
	 * @param that the objecct to be compared
	 * @return -int if this < that
	 *         +int if this > that
	 *         0 if this.equals(that)
	 */
	@Override
	public int compareTo(final Student that)
	{
		return this.firstName.length() -
				that.firstName.length();
	}
}
```

collections:
```java
public class Test
{
	public static void main(final String[] args)
	{
		final String[] strings = {"ab", "xy", "cd"};
		final Integer[] ints = {4, 67, 88, 32, 1};
		final Double[] doubles = {4.6, 65.4, 88.2, 1.5};
		final Character[] chars = {'a', 'b', 'c', 'd'};

		final Student s1;
		final Student s2;
		final Student s3;
		final Student s4;

		s1 = new Student(2001, "wong", 3.7);
		s2 = new Student(2001, "wong", 3.7);
		s3 = new Student(2001, "wong", 3.7);
		s4 = new Student(2001, "wong", 3.7);

		final Student[] students = {s1, s2, s3, s4};	

		
	}

	static <T extends Comparable<T>> T getMax(T[] a)
	{
		T max = a[0];

		for(T i: a)
		{
			if(i.compareTo(max) > 0)
			{
				max = i;
			}
		}

		return max;
	}
}
```
