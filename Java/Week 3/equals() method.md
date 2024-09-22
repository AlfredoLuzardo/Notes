- When comparing objects, java (or a developer) can call its equals() method.

- The Object class has an equals() method, which simply returns whether the two objects have the same address.

- Do not use == with String (or other objects) unless you really do want to compare addresses

- It can be overridden.

```java
@Override
public boolean equals(final Object o)
{
	if(o == null)
	{
		return false; // this. is definitely not equal to null
	}

	// if(o == this)
	// {
	//	return true;
	// }

	if(!(o.getClass().equals(this.getClass()))) // or instanceof
	{
		return false; // these aren't the same class
	}
	// now return true only if you consider the two objects equal
}
```

- Equal objects must have equal hash codes

```java
@Override
public boolean equals(final Object o)
{
	if(o == null)
	{
		return false; // this. is definitely not equal to null
	}

	if(o.getClass().equals(this.getClass())) // or instanceof
	{
		final HockeyPlayer h;
		h = (HockeyPlayer)o;
		return h.teamName.equalsIgnoreCase(this.teamName);	
	}
	return false;
}

@Override
public int hashCode()
{
	return Objects.hashCode(teamName);
}
```

