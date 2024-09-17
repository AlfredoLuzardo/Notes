
**Immutable**: Once a String has been created, it cannot be modified

- The following code simply points s to a new String (the original String, again, cannot be changed):  
	- String s = "hello";  
	- s = "world";

**Comparing Strings**:
- Do not compare strings using ==
- Strings are compared using .equals()
- There is also .equalsIgnoreCase()
- There is also .compareTo() which tells which String is bigger