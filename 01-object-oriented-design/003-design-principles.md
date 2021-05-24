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



## 1.3.2 Separation of Concerns

***Glossaries***

1. COBOL *(programming language)*
2. Fortran *(programming language)*
3. Programming Paradigms
4. Global Data
5. Global Data Access  

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