# Week 3: Design Principles

## Design Principles

---

## 1.3.1 Coupling and Cohesion

***Coupling*** focuses on complexity between a module and other modules.
***Cohesion*** focuses on complexity within a module.  

If a module is highly reliant on other modules, it is called ***tightly coupled***.  
If a module is easy to be connected to other modules, it is called ***loosely coupled***. *(preferred)*  

When evaluating the coupling of a module, there are 3 things to consider:

1. Degree
2. Ease
3. Flexibility

***Degree***

> Degree is the number of connections between the module and others. With coupling, you want to keep the degree small. For instance, if the module needed to connect to other modules, through a few parameters or narrow interfaces, then the degree would be small, and coupling would be loose.

***Ease***

> Ease is how obvious are the connections between the module and others. With coupling, you want the connections to be easy to make without needing to understand the implementations of the other modules.

***Flexibility***

> Flexibility is how interchangeable the other modules are for this module. With coupling, you want the other modules easily replaceable for something better in the future.

***Questions***

What aspects of a lego piece makes it looselt couple to other lego pieces?  
`[  ]` Corresponding pieces are hard to find  
`[✓]` It can be connected to any lego piece *(this is the reusability aspect of coupling)*  
`[✓]` Connecting two legos work flawlessly *(this describes the flexibility that you get from loose coupling)*  
`[✓]` Pieces can be interchanged *(This also describes the flexibility you get from loose coupling)*  

What aspects of a puzzle piece make it tightly coupled to other puzzle pieces?  
`[✓]` Corresponding pieces are hard to find *(poor ease)*  
`[  ]` Pieces are interchangeable  
`[✓]` It can only be connected to specific puzzle pieces *(inflexible)*  

***Cohesion***

> Cohesion represents the clarity of the responsibilities of a module.

If a module performs one task and nothing else or has a clear purpose, the module has ***high cohesion***. *(preferred)*  
If a module tries to encapsulate more than one purpose or has an unclear purpose, the module has ***low cohesion***.

***Questions***

What aspects of a lego piece makes it high cohesion?  
`[✓]` A lego's task is clear, "to connect to other lego" *(a cohesive "piece" will have a clear purpose - high cohesion)*  
`[  ]` Corresponding pieces are easy to find  
`[  ]` It can be connected to any other lego piece  
`[  ]` How snug it fits to corresponding pieces  

What aspects of a puzzle piece makes it low cohesion?  
`[  ]` It can only be connected to specific puzzle pieces  
`[  ]` How snug it fits to corresponding pieces  
`[  ]` Corresponding pieces are hard to find  
`[✓]` Its responsibility is unclear and caries in the pieces *(a true statement that addresses low cohesion)*  

Example in Java

```java
public void get (int controlFlag) {
    switch (controlFlag) {
        case 0:
            return this.humidity;
            break;
        case 1:
            return this.temperature;
            break;
        default:
            throw new UnknownControlFlagException();
    }
}
```

***Questions***

Which of the following is true about `Sensor` class and its cohesion?  
`[✓]` `Sensor` class has low cohesion, since it has two purposes and therefore unclear. *(one purpose is enough for one class. Any more than that takes away from cohesion)*  
`[  ]` `Sensor` class has high cohesion, since its purpose is clear.  
`[  ]` `Sensor` class has low cohesion, since its `get` method is not straightforward.  

Which of the following is true about coupling to the Sensor class?  
`[  ]` `Sensor` class has low coupling, since its purpose is clear.  
`[  ]` `Sensor` class has tight coupling, since it has two purposes and therefore unclear.  
`[✓]` `Sensor` class has tight coupling, since its `get` method is not straightforward. *(A user of the `get` method will have to open up `Sensor` to see how it works. That's not loose coupling)*  

***Solution (as UML class diagram)***

```none
                       .-----------------------. 
                       |     «interface»       |
                       |       IAnimal         |
                       '-----------------------'
                       |                       |
                       '-----------------------'
                       | +get()                |
                       '-----------------------'
                                   △
                                   :
           ....................................................
           :                                                  :
  .----------------.                               .-------------------.
  | HumiditySensor |                               | TemperatureSensor |
  '----------------'                               '-------------------'
  |                |                               |                   | 
  '----------------'                               '-------------------'
  | +get()         |                               | +get()            |
  '----------------'                               '-------------------'
```

***Question***

Suppose you are working on a company that manufactures an automated watering program.  
You are asked to evaluate the complexity of the following code:  

```java
public class Globals {
    public static double Pressure = 0.0;
}

public class LawnSprinkler {
    public void sprinkle() {
        this->_pressure = Global.Pressure;
        this->turnOnWaterPump(this->_pressure);
    }

    private void turnOnWaterPump(double pressure) {
        // implementation
    }

    // .. Other parts of the class
}
```

What can you say about `LawnSprinkler`\'s cohesion?  
`[✓]` It has one clear purpose, to sprinkle the lawn. Therefore it is highly cohesive.  
*(The class is highly cohesive because it is completely focused on sprinkling. `turnOnWaterPump()`*  
*is part of that responsibility, although if it was outsourced to another class, then users of*  
*`sprinkle()` would have no idea!)*  

What can you say about the coupling of `LawnSprinkler`\`s `sprinkle` method?  
`[  ]` It has a small degree due to having no parameter. Therefore it is loosely coupled to its caller.  
`[  ]` It has one clear purpose, to sprinkle the lawn. Therefore it is loosely coupled.  
`[✓]` Despite having no parameter, it lacks ease due to its use of globals. Therefore tightly coupled.  
*(The reason why you should avoid using globals is that you never know what other modules use*
*or modify them. This makes methods that use them have low ease which makes them tightly coupled.)*

## 1.3.2 Separation of Concerns

One goal of software design priciples si to help create a system that is

* flexible
* reusable
* maintainable

***Concern***

> A concern is a very general notion, basically it is anything that matters in providing a solution to a problem.
>  
> How these abstractions are implemented in the software can lead to more concerns. Some of these concerns may involve:  
>
> * What information the implementation represents
> * What it manipulates
> * What gets presented at the end

## 1.3.3 Information Hiding

## 1.3.4 Conceptual Integrity

## Generalization Principles

---

## 1.3.5 Inheritance Issues

## Modelling Behaviour

---

## 1.3.6 UML Sequence Diagram

## 1.3.7 UML State Diagram

## Model Checking

---
## 1.3.8 Model Checking