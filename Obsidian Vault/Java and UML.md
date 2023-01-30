# Java
- use camel case
- capitalize the first letter of a Class, but DO NOT do it to a method

Scope of Access
--
- private: only this class
- protected: this class and its children
- public: everyone
- default: inside package

# [[UML]]
```plantuml
class Walker{
	Legs[] legs;
	Position pos;
	Velosity vel;
	void walkTo(Position p);
}
class Cat extends Walker{
	Legs[4] legs;
	String voice;
	void yelling();
}

```
```java
class Walker{
	Legs[] legs;
	Position pos;
	Velosity vel;
	void walkTo(Position p);
}
class Cat extends Walker{
	Legs[4] legs;
	String voice;
	void yelling();
}
```

In this class, we <a>DO NOT</a> write attributes the way the picture above.
Instead of `Legs[] legs` like what it is in java, we use `legs: Legs[]`

Key: attributes BEFORE types

	All class should have three boxes stacked together, representing Class, Attributes, and Methods. Or, only the box represents Class, if you want to hide the detail.
