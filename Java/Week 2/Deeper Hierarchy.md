```java
class Animal
{
	private double weightKg;
	Animal(final double weightKg)
	{
		this.weightKg = weightKg;
	}

	protected double getWeightKg()
	{
		return weightKg;
	}

	protected void setWeightKg(final double kg)
	{
		this.weightKg = kg;
	}
}
```
```java
class Dog extends Animal
{
	private final String name;

	Dog(final double weightKg, final String name)
	{
		super(weightKg);
		this.name = name;
	}

	protected String getName()
	{
		return name;
	}
}
```
```java
public class Pitbull extends Dog
{
	private boolean trained;

	Pitbull(final double weightKg, final String name, final boolean trained)
	{
		super(weightKg, name);
		this.trained = trained;
	}

	protected boolean isTrained()
	{
		return trained;
	}

	protected void setTrained(final boolean trained)
	{
		this.trained = trained;
	}
}
```

