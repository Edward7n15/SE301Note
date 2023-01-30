Dividing whole things into parts.
```
class Car{
	Color color;
	Engine engine;
	Headlight hl1;
	Headlight hl2;
	Window w1;
	Window w2;
	...
	Tire[] tires;
}
```
	This is also Abstraction and Encapsulation.
```
class Tire{
	boolean forWinter;
}
```
Is Tire class Fixed or Dynamic? Will it be garbage collect? Does it share the life time with Car?
Strongly own: Tire is <a>fixed</a>, it will be garbage collected when Car was collected.
Own: Tire is <a>dynamic</a>, it will stay even if Car is collected.

Data parts
--
- fixed or dynamic number (changeable of the number)
	For a node of a linked list, what and how many nodes the pointer points to is DYNAMIC. (0...1)
- sharing of parts (share or hardcode)
	If the Color of a Car is shared, and there are something else is in the same color, then everything in the color will change when you modify the Color class.
- life time of parts (strongly own?)

In java
--
show the relationship between classes.