## **1.2.1 Models: Bridging Concepts and Solutions**
<br>

Glossaries:
1. Top Down Programming
2. Object-Oriented Analysis
3. Object-Oriented Design
4. Unified Modeling Language (UML)
5. Object-Oriented Modeling
<br>
<br>

## **1.2.2 Languages Evolution**
<br>

Glossaries
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

<br>

**Imperative Paradigm**<br>
    
    COBOL and Fortran followed an imperative paradigm which broke up large programs into smaller programms called subroutines, which are like methods in Java.

**Abstract Data Type**<br>

    An abstract data type is a data type that is defined by programmer and not built into the language. 
    An abstract data type is essentially a grouping of related information that is denoted with a type.
    It was a way to organize data in a meaningful way.

The goal of object-oriented design is to:
* Make an abstract data type easier to write
* Structure a system around abstract data types called classes
* Introduce the ability for an abstract data type to extend another
<br>

Advantages of object-oriented design

    The system will mimic the structure of the problem
<br>

Popular object-oriented languages:
1. Java
2. C++
3. C#
<br>

There are many systems that still use the older languages and design paradigms.
<br>
<br>

## **Four Design Principles**
---
## **1.2.3 Abstraction**
<br>

**Abstraction**<br>

    Abstraction is the idea of simplifying a concept in the problem domain to its essntials within some context.
    Abstraction allows you to better understand a concept by breaking it down into a simplified description that
    ignores unimportant details.
<br>

**Rule of Least Astonishment**<br>

    The abstraction captures the essential attributes and behavior for a concept with no surprises and no definitions
    that fall beyond its scope. You don't want to surprise anyone trying to understand your abstraction with irrelevant
    characteristics.
<br>

**Examples of abstraction of a student**<br>

Some of the essential characteristics of a student: 
* The courses they are currently taking
* Their grades in each course
* Their student ID number

Courses, grades, and student ID are the ***attributes***.<br>
The attributes do not disappear over time although the values may change since they are essential characteristics of a student.

In addition to attributes, an abstraction should describe a concept's ***basic behaviour***.
For a ***student***, those behaviours would be:
1. Studying
2. Doing assignments
3. Attending lectures

These are the ***responsibilities***
<br>
<br>

Abstractions are formed within a specific context for perspective and have to be carefully decided what is relevant. If the purpose of the system or the problem changes, abstractions can be updated accordingly.<br>

    Abstractions are not a fixed creation, but are a direct result of the problem for which created them.

***Questions***<br>
1. What object-oriented programming construct should be used to represent a concept in the problem domain?<br>
    * Class *(Classes are the primary way that the problem domain is represented in object-oriented paradigm. Objects are instances of classes)*

2. Give examples of attributes for a "house cat" from the perspective of a cat owner.
    * name, color, favorite nap location, hunger level, microchip number, etc.

3. Give examples of behaviors for a "house cat" from the perspective of a cat owner.
    * napping, grooming, catching mice in the house, eating, using the litter box, etc.
      *Each of these could be implemented as a method in the house cat class*

4. Try creating a dog abstraction for the software space! Remember to identify both attributes and behaviors.
    * Attributes: dog's breed, size, hair, ears, color
    * Behaviours: sleeping, eating, doing tricks
<br>
<br>

## **1.2.4 Encapsulation**
<br>

## **1.2.5 Decomposition**
