
- Method overriding is not the same as overloading

- Means a child (or grandchild, etc.) redefines a method that was already defined higher in the hierarchy

- The signature must be the same

- Use the @Override annotation in the new version of the method; if you are in fact not overriding a method, the compiler will tell you

- Static methods and private methods cannot be overridden

- The new methods visibility must be the same or wider than the parent version


**ANIMAL CLASS**:

```java
public void speak()
{
	System.out.println("Speaking");
}

protected void move()
{
	System.out.println("Moving");
}
```

**DOG CLASS**:

```java
@Override
public void speak()
{
	System.out.println("Woof Woof");
}

@Override
protected void move()
{
	System.out.println("Running");
}
```

**DOLPHIN CLASS**:

```java
@Override
public void speak()
{
	System.out.println("Eeee eee");
}

@Override
public void move()
{
	System.out.println("Swimming");
}
```

**MAIN**:

```java
a1 = new Animal(200.0);  
a2 = new Dog(30.0, "Rex");  
a3 = new Pitbull(50.0, "Rocky", true);  
a4 = new Dolphin(300.0, false);

//RUNTIME
a1.speak(); // Speaking
a1.move(); // Moving

a2.speak(); // Woof Woof
a2.move(); // Running

a3.speak(); // Woof Woof
a3.move(); // Running

a4.speak(); // Eeee eee
a4.move(); // Swimming
```

