# Week 2: Object-Oriented Modeling

## **1.2.1 Models: Bridging Concepts and Solutions**

***Glossaries***

1. Top Down Programming
2. Object-Oriented Analysis
3. Object-Oriented Design
4. Unified Modeling Language (UML)  
5. Object-Oriented Modeling  

## **1.2.2 Languages Evolution**

***Glossaries***

1. COBOL *(programming language)*
2. Fortran *(programming language)*
3. Programming Paradigms
4. Global Data
5. Global Data Access
6. Subprograms
7. Algol 68 *(programming language)*
8. Pascal *(programming language)*
9. Local Variables
10. Nested Procedures
11. C *(programming language)*
12. Modula-2 *(programming language)*

***Imperative Paradigm***

> COBOL and Fortran followed an imperative paradigm which broke up large programs into smaller programms called subroutines, which are like methods in Java.

***Abstract Data Type***

> An abstract data type is a data type that is defined by programmer and not built into the language. An abstract data type is essentially a grouping of related information that is denoted with a type. It was a way to organize data in a meaningful way.

The goal of object-oriented design is to:

* Make an abstract data type easier to write
* Structure a system around abstract data types called classes
* Introduce the ability for an abstract data type to extend another

Advantages of object-oriented design

> The system will mimic the structure of the problem

Popular object-oriented languages:

1. Java
2. C++
3. C#

There are many systems that still use the older languages and design paradigms.

## **Four Design Principles**

---

## **1.2.3 Abstraction**

***Abstraction***

> Abstraction is the idea of simplifying a concept in the problem domain to its essntials within some context. Abstraction allows you to better understand a concept by breaking it down into a simplified description that ignores unimportant details.

***Rule of Least Astonishment***

> The abstraction captures the essential attributes and behaviour for a concept with no surprises and no definitions that fall beyond its scope. You don't want to surprise anyone trying to understand your abstraction with irrelevant characteristics.

***Examples of abstraction of a student***

Some of the essential characteristics of a student:

* The courses they are currently taking
* Their grades in each course
* Their student ID number

Courses, grades, and student ID are the ***attributes***.  
The attributes do not disappear over time although the values may change since they are essential characteristics of a student.

In addition to attributes, an abstraction should describe a concept's ***basic behaviour***.
For a ***student***, those behaviours would be:

1. Studying
2. Doing assignments
3. Attending lectures

These are the ***responsibilities***  

Abstractions are formed within a specific context for perspective and have to be carefully decided what is relevant. If the purpose of the system or the problem changes, abstractions can be updated accordingly.  

> Abstractions are not a fixed creation, but are a direct result of the problem for which created them.

***Questions***

1. What object-oriented programming construct should be used to represent a concept in the problem domain?
    * Class *(Classes are the primary way that the problem domain is represented in object-oriented paradigm. Objects are instances of classes)*

2. Give examples of attributes for a "house cat" from the perspective of a cat owner.
    * name, color, favorite nap location, hunger level, microchip number, etc.

3. Give examples of behaviors for a "house cat" from the perspective of a cat owner.
    * napping, grooming, catching mice in the house, eating, using the litter box, etc.
      *Each of these could be implemented as a method in the house cat class*

4. Try creating a dog abstraction for the software space! Remember to identify both attributes and behaviors.
    * **Attributes**: dog's breed, size, hair, ears, color
    * **Behaviours**: sleeping, eating, doing tricks

## **1.2.4 Encapsulation**

***Encapsulation***

> Encapsulation forms a self-contained object by bundling the data, and functions it requires to work, exposes an interface whereby other objects can access and use it, and restricts access to certain inside details.

Encapsulation involves 3 ideas:

1. Bundle attribute values, data, behaviour, or functions that manipulate those values together into a self-contained object
2. Expose certain data and functions of an object, which can be accessed from other objects
3. Restrict access to certain data and functions to only within an object

Why encapsulation?

1. Encapsulation helps with data integrity
2. Encapsulation can secure sensitive information
3. Encalsulation helps with software changes

***Questions***

1. Choose the attributes that will be **encapsulated** in each of the above objects
    * **Student** object: *degree program of the student*
    * **Course** object: *list of students taking the course*
    * **Professor** object: *list of courses the professor teaches*

2. What advantages come from encapsulation?
    * Security is increased due to restricted and controlled access to attributes and methods
    * Changing the software is easier because related data and code are located in the same place
    * Reusability is increased because the interface of a class can stay the same even if its internal implementation changes
        *(this is called **refactoring** and it will be easier to do with proper encapsulation)*

***Glossaries***

1. Bundle
2. Data
3. Functions
4. Expose
5. Restrict
6. Methods
7. Interface
8. Restricted
9. Black box thinking
10. Abstraction barrier  

## **1.2.5 Decomposition**

***Decomposition***

> Decomposition is taking a whole thing and dividing it up into different parts. Or, on the flip side, taking a bunch of separate parts with different functionalities and combining them together to form a whole. Decomposition allows you to further break down problems into pieces that are easier to understand and solve.

***Questions***

1. What are some objects that you might get by decomposing a car?
    * Wheels, a steering wheel, a windshield, a gas pedal, engine, a fuel pump
        *(the chosen objects to use in software will depend on the **context**)*

2. Which of these car "parts" has a dynamic number?
    * Passengers *(a car can accommodate a **dynamic** number of passengers)*

3. Returning to our example of a car, can you think another example of a part that contains another part?
    * A headlamp contains a bulb
    * The wheel contains a rim and a tyre
    * An engine contains many things, like pistons and spark plugs
    * Instrument panel contains a fuel gauge, an odometer, and a speedometer

4. Consider the lifetime of a car, can you think of one part that has a closely-related lifetime and one part that does not?
    * Closely-related lifetime: car frame, engine *(when the engine goes, so does the car)*
    * No closely-related lifetime: wheels *(can be replaced many times over the course of a car's life)*

***Glossaries***

1. Fixed number
2. Dynamic number
3. Parts containing parts
4. Lifetime
5. Sharing

## **1.2.6 Generalisation**

***Generalisation***

> Generalisation is frequently used when designing algorithms, which are meant to be used to perform the same action on different sets of data. We can generalise the actions into its own method, and simply pass it through a different set of data through arguments.

When a ***child class*** inherits from a ***parent class***, the child class will have the attributes and behaviours of the parent class.
Common attributes and behaviours are placed in parent class.

> In standard terminology, a parent class is known as a superclass and a child class is called the subclass

***Question***

1. Inheritance is used to describe the relationship between classes. What are the three ways in which this relationship is advantageous?
    * Subclasses that inherit from the same superclass include attributes and behaviours from the superclass  
        *(This is an easy way to share attributes and behaviour among related classes)*
    * Changes can be made easily and quickly to a large group of subclasses by making changes to the superclass they inherit from  
        *(Changes to the superclass apply to all the subclasses unless the subclasses overrides the superclass)*
    * Code can be reused through inheritance, which means we do not need to re-implement behaviours that already exist  
        *(This is one way that you can apply D.R.Y (Don't Repeat Yourself)*

***Glossaries***

1. Inheritance
2. Repeated
3. Common
4. Shared characteristics
5. Parent class
6. Child class
7. D.R.Y (Don't Repeat Yourself)  

## **Expressing Design Structure in Java & UML Class Diagrams**

---

## **1.2.7 Abstraction in Java and UML**

Example of ***CRC card*** and ***class diagram*** representation of **`food class`**

***Example 1***  
Converting class diagram into Java code

```none
CRC card
.------------------------------------.
| Food                               |   <--- class name
'-----------------------.------------'
| Know grocery ID       |            |
| Know name             |            |
| Know manufacturer     |            |
| Know expiry date      |            |
| Know price            |            |
| Check if on sale      |            |
'------------------------------------'
        ^                      ^
  Responsibility         Collaborator
  

Class diagram
.---------------------------.
| Food                      |   <--- class name
'---------------------------'          the same as class name in Java class
| groceryID: String         |
| name: String              |
| manufacturer: String      |   <--- properties
| expiryDate: Date          |          equivalent to member variables 
| price: double             |          in Java class and define the
'---------------------------'          attributes of the abstraction
| isOnSale(): boolean       |   <--- operations
'---------------------------'          equivalent to the methods in
                                       Java class and define the behaviour
                                       of the abstraction
```

The equivalent Java code

```java
// class name turns into class
public class Food {
    // properties turn into member variables
    public String groceryID;
    public String name;
    public String manufacturer;
    public Date expiryDate;
    public double price;

    // operation turns into method
    public boolean isOnSale
    () {

    }
}
```

***Example 2***  
Converting Java code into class diagram

```java
public class ClickCounter {
    private int count;

    public ClickCounter() {
        count = 0;
    }

    public void click() {
        count++;
    }
    public void setClickCount(int ClickCount) {
        count = clickCount;
    }

    public int getClickCount() {
        return count;
    }
}
```

```none
.--------------------------------------.
| ClickCounter                         |
'--------------------------------------'
| count: int                           |
'--------------------------------------'
| click(): void                        |
| setClickCount(clickCount: int): void |
| getClickCount(): int                 |
'--------------------------------------' 
```

> CRC card does not show clear separation between ***properties*** and ***operations***. See how both are combined in ***responsibility*** section, which may sometimes cause ambiguity. ***Class diagram*** represents code better.

***Glossaries***

1. UML Diagrams
2. UML Class Diagram (Class Diagram)
3. Abstraction
4. CRC

## **1.2.8 Encapsulation in Java and UML**

Ideas of encapsulation:

1. Bundle data and functions that manipulate the data, into a self-contained object
2. Expose certain data and functions of that object, which can be accessed from other objects
3. Restrict access to certain data and functions to only within that object

Example of encapsulation of Student class using UML Class diagram.  
***+*** sign indicates that a method or attribute is public.  
***-*** sign indicates that a method or attribute is private.

```none
.--------------------------------------.
| Student                              |
'--------------------------------------'
| -gpa: float                          |
| -degreeProgram: String               |
'--------------------------------------'
| +getGPA(): float                     |
| +setGPA( float ): void               |
| +getDegreeProgram(): String          |
| +setDegreeProgram( String ): void    |
'--------------------------------------' 
```

UML diagram that displays proper encapsulation for a `Driver` class  
(The attributes are hidden, but there are methods exposed to make changes)

```none
.--------------------------------------.
| Driver                               |
'--------------------------------------'
| -licenseID: String                   |
| -car: Car                            |
'--------------------------------------'
| +getLicenseID(): String              |
| +setLicenseID( float ): void         |
| +getCar(): Car                       |
| +setCar( Car ): void                 |
'--------------------------------------' 
```

***Getter Methods***

> Getter methods are methods that retrieve data, and their names typically begin with get and end with the name of the attribute whose value you will be returning.
>
> Getters often retrieve a private piece of data

***Setter Methods***

> Setter methods change data, and their names typically begin with set and end with the name of the variable you wish to set.
>
> Setters are used to set a private attribute in a safe way.

Java code example  

```java
public class Student {
    private float gpa;
    private String degreeProgram;

    public float getGPA() {
        return gpa;
    }

    public void setGPA(float newGPA) {
        gpa = newGPA;
    }

    public String getDegreeProgram() {
        return degreeProgram;
    }

    public void setDegreeProgram( String newDegreeProgram ) {
        degreeProgram = newDegreeProgram;
    }
}
```

## **1.2.9 Decomposition in Java and UML**

***Decomposition***

> Taking a **whole** thing and dividing it up into different **parts**. Or, on the flip side, taking a bunch of separate parts with different functionalities and combining them together to form a whole. Decomposition allows you to further break down problems into pieces that are easier to understand and solve.

There are three types of relationships found in decomposition:

* Association
* Aggregation
* Composition

***Association***

> Association is "some" relationship. This means that there is a loose relationship between two objects. These objects may interact with each other for some time.

Object pairs that best describe an association

* Kitten - Yarn
* Student - Sport
* Food - Wine

## **1.2.10 Generalisation with Inheritance in Java and UML**

## **1.2.11 Generalisation with Interfaces in Java and UML**
