
```java
@Override
public int hashCode()
{
	return Objects.hashCode(numGoals);
}
```

- Whenever you override equals(), you must also override hashCode()
- An object should return the same hashCode if called multiple times in running an application
- The Object class has a hashCode() method, which simply returns a hash of the object's address
- It can be overridden

**RULE**: EQUAL OBJECTS MUST RETURN EQUAL HASHCODES


