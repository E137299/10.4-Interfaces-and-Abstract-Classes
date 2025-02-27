# 10.4 Interfaces and Abstract Classes

### **Objective**  
Students will create a Java program in which they define their own scenario and implement the following concepts:  
- **An Interface** (with at least three methods)  
- **An Abstract Class** (that implements the interface and includes additional abstract methods)  
- **Two Subclasses** (that extend the abstract class and provide concrete implementations)  
- **A Third Unrelated Class** (that implements the interface but is not related to the abstract class hierarchy)  

### **Instructions**  
1. **Create a Scenario**:  
   - Choose a real-world or fictional scenario where multiple objects share common behavior but also have distinct characteristics.  
   - Example ideas:  
     - A **Vehicle System** where `Vehicle` is an abstract class, `Car` and `Bike` are subclasses, and `Drone` is an unrelated class implementing a `Movable` interface.  
     - A **Game Character System** where `Character` is an abstract class, `Warrior` and `Mage` are subclasses, and `Monster` is an unrelated class implementing an `Attackable` interface.  
     - A **Smart Home System** where `Appliance` is an abstract class, `Refrigerator` and `AirConditioner` are subclasses, and `SmartSpeaker` is an unrelated class implementing a `Controllable` interface.  

2. **Define an Interface (`YourInterface`)**  
   - The interface should include at least **three method signatures** that describe behaviors common across multiple classes.  
   - Example: A `Movable` interface might include:  
     ```java
     public interface Movable {
         void startMoving();
         void stopMoving();
         int getSpeed();
     }
     ```  

3. **Create an Abstract Class (`YourAbstractClass`)**  
   - Implement the interface in an abstract class.  
   - Define at least **one abstract method** that subclasses must implement.  
   - Include **instance variables** and **at least one concrete method**.  
   - Example:
     ```java
     public abstract class Vehicle implements Movable {
         protected String name;
         protected int speed;
         
         public Vehicle(String name) {
             this.name = name;
             this.speed = 0;
         }

         @Override
         public void startMoving() {
             this.speed = 10;
             System.out.println(name + " starts moving.");
         }

         @Override
         public int getSpeed() {
             return speed;
         }

         // Abstract method to be implemented by subclasses
         public abstract void honk();
     }
     ```  

4. **Create Two Subclasses (`SubClass1` and `SubClass2`)**  
   - These should extend the abstract class and **implement its abstract method(s)**.  
   - They can have additional attributes and behaviors.  
   - Example:
     ```java
     public class Car extends Vehicle {
         public Car(String name) {
             super(name);
         }

         @Override
         public void honk() {
             System.out.println(name + " honks: Beep Beep!");
         }
     }

     public class Bike extends Vehicle {
         public Bike(String name) {
             super(name);
         }

         @Override
         public void honk() {
             System.out.println(name + " rings the bell: Ring Ring!");
         }
     }
     ```  

5. **Create a Third Unrelated Class (`UnrelatedClass`)**  
   - This class **should not extend the abstract class** but **should implement the interface** directly.  
   - Example:
     ```java
     public class Drone implements Movable {
         private int speed;

         public Drone() {
             this.speed = 0;
         }

         @Override
         public void startMoving() {
             this.speed = 20;
             System.out.println("Drone is flying at speed: " + speed);
         }

         @Override
         public void stopMoving() {
             this.speed = 0;
             System.out.println("Drone has stopped.");
         }

         @Override
         public int getSpeed() {
             return speed;
         }
     }
     ```  

6. **Write a `Main` Class to Test Your Code**  
   - Create objects of each class and call their methods.  
   - Example:
     ```java
     public class Main {
         public static void main(String[] args) {
             Car myCar = new Car("Toyota");
             Bike myBike = new Bike("Mountain Bike");
             Drone myDrone = new Drone();

             myCar.startMoving();
             myCar.honk();
             
             myBike.startMoving();
             myBike.honk();

             myDrone.startMoving();
             System.out.println("Drone speed: " + myDrone.getSpeed() + " km/h");
             myDrone.stopMoving();
         }
     }
     ```  

