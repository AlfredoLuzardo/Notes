
- **Categories**
	- **Checked** Exceptions:
		- must be declared; must be wrapped in try/catch
		- used when things are likely to go wrong, and can be handled: (this forces other code to use try/catch and forces the thrower to declare that it throws; checked at compile time)
	- **Unchecked** Exceptions:
		- optionally can be in try/catch (aka runtimeException)
		- used when things are unlikely to go wrong
	- **Custom** Exceptions:
		- make your own (checked or unchecked) exceptions
		- used only if they add lots of readability and value, otherwise stick to the normal Java Exception classes


**Checked Exception**:

creating checked:

```java
class IllegalChessMoveException extends Exception
{
	IllegalChessMoveException(final String message)
	{
		super(message);
	}
}
```

must declare it throws:

```java
class Pawn
{
	public void move(char startFile,
					 int startRow,
					 char endFile,
					 int endRow) throws IllegalChessMoveException
	{
		if(endRow <= startRow)
		{
			throw new IllegalChessMoveException("illegal pawn move");
		}
	}
}
```

must try/catch:

```java
class Chess
{
	public static void main(final String[] args)
	{
		Pawn pawn = new Pawn();
		try
		{
				pawn.move('a', 2, 'a', '7');
		}
		catch(IllegalChessMoveException e)
		{
			System.out.println(e.getMessage());
		}
	}
}
```


**Unchecked Exception**

creating unchecked:

```java
class IllegalChessMoveException extends RuntimeException
{
	IllegalChessMoveException(String message)
	{
		super(message);
	}
}
```

throws declaration optional:

```java
class Pawn
{
	public void move(char startFile,
					 int startRow,
					 char endFile,
					 int endRow)
	{
		if(endRow <= startRow)
		{
			throw new IllegalChessMoveException("illegal pawn move");
		}
	}
}
```

try/catch optional:

```java
class Chess
{
	public static void main(final String[] args)
	{
		Pawn pawn = new Pawn();
		pawn.move('a', 2, 'a', '7');
	}
}
```

**Class Hierarchy**

- Throwable:
	- Anything with this parent, can be thrown
- Error:
	- the JVM that runs Java programs has a problem with hardware or software (e.g. out of memory)
- Exception Checked:
	- program specific problem out of the programmers control (e.g. a necessary file has been deleted; a network connection to a remote database is broken)
- Runtime Exception (Unchecked):
	- A problem made by the programmer needs to be fixed (e.g. tried to call toUpperCase() on a null String reference): any resulting crash is good because it draws our attention and we will fix the coding error


**Exception Handling**

- main() should not throw any exceptions

- The finally { } block is always executed (even if try/catch return)

- The compiler forces us to handle checked exceptions (by try/catch or by declaring and throwing them)
- The compiler does not force us to handle unchecked exceptions; don't try/catch these; let them crash the program and thus draw our attention to make repairs

- To handle an exception from a catch block, we can do a number of different things:
	- Handle it directly in that catch block
	- Call a handler method from the catch block
	- Print the stack trace in the catch block (ok for development, not for production)