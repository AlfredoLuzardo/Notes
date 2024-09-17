If and only if your class does not provide any constructor, Java will (invisibly) create one for you:

```java
// What you typed
class Dog extends Animal
{

}
// What java creates
class Dog extends Animal
{
	Dog()
	{
		super();
	}
}
```

This is called the "default constructor" and it takes zero arguments and only calls super()