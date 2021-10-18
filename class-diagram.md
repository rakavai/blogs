# UML - Class Diagram

Let's start the class diagram from the high-level, and we will dig into low level.

On high-level there is two things we can see-

 * Class block - The Box Shape
 * Connecting line among the class

Based on the line type we can figure how the entities are connected with each other. Let's first go thorough different
type line type for the relation type.

## Connector for different type relationship

### 1. Solid arrow line is for Inheritance

![Solid arrow line is for Inheritance](./diagram/inheritance.png)

The direction of the arrow is from child class to parent class. The arrow head is unfilled.
Just to put emphasis, the child class is just a specific type of parent class and can be replaced with one another.

### 2. Broken arrow line is for Interface-Implementation class

![Dashed arrow line is for Interface](./diagram/interface.png)

This arrow is used to show interface implementation. The arrow direction is from the implementation class to interface.
The arrow head is unfilled.