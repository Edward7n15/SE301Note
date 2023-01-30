# Purpose:

- Express OO designs visually
- Programming language independent
- Communicate, evaluate , and resue designs
- Make design intent more explicit
- Think about degisn before coding (bigger picture)

# Box and Scope
--
```plantuml
skinparam classAttributeIconSize 0
class Frame{
	
	-x: Integer
	-y: Integer
	
	+ Frame(String name, int x, int y);
	- moveTo(int x, int y);
}
```


# Relationship
```plantuml
Octopus"1" -> "0..*"Tentacle : has
Octopus"1" -> "0..*"Snail : eats
```
```plantuml
Food "0..*" -- "0..*" Wine : goes well with
```
	a Food object is associated with 0 or more Wine object, vice versa.

## Strong or Wear "has-a"?
*has-a* means classA has a variable which is in classB
### Composition

Strong relationship: be collected along with the parent
```plantuml
Hand "1" *-- "0..*" Finger
```
	More than that, the Finger is EXCLUSIVELY belong to Hand, which means other objects can not have THIS Finger. Other objects may have other Finger instead, or have a copy of the Finger.
### Aggregation

Dynamic relationship: 
```plantuml
Section "0..*" o-- "0..*" Student
Location "1" --o "0..*" Frame
Frame "0..*" o-- "1" Size
```
	Generalize Location and Size, share them with Frame. Also called, "Fixed Number of Aggregated objects".
*notice:* the side with dimond is the parent

### Association
```plantuml
ClassA - ClassB
```
- caller - callee
- parameter
- no relationship in code but in real life
## [[Inheritance]]
```plantuml
Shape <|-- Circle
Shape <|-- Square
```
IS-A relationship: empty arrow
*notice*: NUMBERS are not inportant here since we are talking about a general concept of belonging. 

Liskov substitution principle
	an instance of the subclass should be substitutable anywhere a reference to a superclass object is used.
```java
Shape s;
s = new Circle(); // instance of subclass
Location l = s.getLocation(); // superclass method
```

When you think it is an imapproperiate inheritance, try
- hide the super method by overwriting it
- use Aggregation instead
- restructure the super class