Bundling data with access functions. The user don't need to know "how".

<a>Information hiding criterion</a>: hide chageable internal details from the outside world, but reveal assumptions through interface

***abstract data type*** is an example of encapsulation.

In java
--
Class is an implementation of Encapsulation
- access control for attributes and method (public / private)
- access is not the same as visibility (you can see it does not mean you can manipulate it)
- "design by contract"
	- public interface represents a <a>contract</a> between the developer who <a>implements</a> the class and the developer who <a>uses</a> the class.

```java
public class Frame{
	private datatype varName; // attribute
	public Frame(arg){} // constructor
	public returntype methodname(arg){} // method
}
```
