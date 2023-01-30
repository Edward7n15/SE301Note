- general part
	- a base class (superclass) defines the attributes and methods to be shared
- specific part
	- a derived class (subclass) is endowed with the attributes and methods of its base class
	- a subclass may <a>extend</a> a superclass by adding attributes and methods, or <a>overriding</a> an existing method

a way of [[Generalization]]

using the keyword `extends`

```java
public class Shape{
	protected Location loc;
	public Shape(){...}
	public void setLoc(Location p){...}
	public Location getLoc(){...}
}

public class Circle extends Shape{
	private int diameter; // adding new attribute
	public Circle(){...} // including super(), which calls the constructor of Shape
	public void setDiameter(int d){...} // adding new method
}
```