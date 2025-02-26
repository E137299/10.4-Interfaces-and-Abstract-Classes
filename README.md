# 10.4 Interfaces and Abstract Classes

## Objective
The objective of this assignment is to create a shape hierarchy in Java using interfaces, abstract classes, and concrete classes. The application should allow users to create different shapes, calculate their area, and display their properties.

## Instructions

1. **Create an Interface `Shape`**
    - Methods:
        - `double getArea()`: Returns the area of the shape.
        - `void display()`: Displays the properties of the shape.

2. **Create an Abstract Class `TwoDimensionalShape` that Implements `Shape`**
    - Fields:
        - `String color`
    - Constructor:
        - Accepts a `String` parameter for the color.
    - Methods:
        - Implement `display()` to print the color of the shape.
        - `String getColor()`: Returns the color of the shape.

3. **Create Concrete Classes `Circle` and `Rectangle` that Extend `TwoDimensionalShape`**
    - **Class `Circle`**
        - Fields:
            - `double radius`
        - Constructor:
            - Accepts `String` color and `double` radius.
        - Methods:
            - Implement `getArea()`: Returns the area of the circle.
            - Override `display()` to print the radius and area of the circle.

    - **Class `Rectangle`**
        - Fields:
            - `double width`
            - `double height`
        - Constructor:
            - Accepts `String` color, `double` width, and `double` height.
        - Methods:
            - Implement `getArea()`: Returns the area of the rectangle.
            - Override `display()` to print the width, height, and area of the rectangle.

4. **Create a `Main` Class with a `main` Method**
    - The `main` method should:
        - Create instances of `Circle` and `Rectangle`.
        - Display their properties and areas.

## Sample Output
```
Circle:
Color: Red
Radius: 5.0
Area: 78.53981633974483

Rectangle:
Color: Blue
Width: 4.0
Height: 6.0
Area: 24.0
```

## Submission Instructions
- Submit your Java source files (`Shape.java`, `TwoDimensionalShape.java`, `Circle.java`, `Rectangle.java`, and `Main.java`).
- Ensure your code is well-documented with comments explaining the functionality of each method and class.
- Test your application thoroughly to ensure it calculates areas correctly and displays properties as expected.

## Grading Criteria
- Code correctness and functionality: 50%
- Use of interfaces, abstract classes, and concrete classes: 30%
- Code readability and documentation: 10%
- User interface and experience: 10%
