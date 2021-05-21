# Week 1: Object-Oriented Analysis and Design

## **1.1.1 Welcome to Software Design and Architecture**

## **1.1.2 Software Architect and Design Roles in Industry**

## **1.1.3 Object-Oriented Modeling**

## **1.1.4 Software Requirements, Conceptual and Technical Designs**

***Questions***

1. *"As a learner, I want to search for relevant courses through a search page."*  
Can you recognize potential objects or components arising from this requirement?  
    * Learner
    * Course
    * Search page

2. Which of the following is a responsibility of a Search Page?  
    * Search. *(One of the responsibilitiwes of the search page is to search! Responsibilities are often the verbs in user stories such as this one)*

3. What other components might the Search Page component relate to?  
    * Result Page *(The search page and result page work together to give the student an interactive experience. They are collaborators!)*
    * Input Field *(The input field is probably another object or component, and it definitely works with the search page, so it must be a collaborator!)*
    * Search Button *(The searcg button is an object that works with the search page: in other words, a collaborator)*

***Components***

> Components turn into collections of functions, classes, or other components. These pieces then represent a much simpler problem that the developers can individually implement.  

### **Expressing Requirements with User Stories**

***General structure***

> As a ..., I want to ... so that ...

1. *First blank*: user role; clarifies who wants to use this feature
2. *Second blank*: goal that the user role wants to achieve; some features that you want to implement
3. *Third blank*: the reason why the user role wants this goal. Sometimes omitted if the benefits are clear and generally known

***Example:***

> As an online shopper, I want to add an item to my shopping cart, so that I can purchase it.

1. *Nouns* correspond to objects in your software
    **online shopper**, **item**, **shopping cart**
2. *Verbs* correspond to connection between objects
    **add**, **purchase**

### **Categories of Objects in Design**

***Entity Objects***

> Correspond to some real-world entity in the problam space.  
> Examples: chair, book, table

***Boundary Objects***

> Objects which sit at the boundary between systems; objects that deal with another software system.  
> Example: user interface  

***Control Objects***

> Objects which are responsible for coordination, i.e. to coordinate the activities of many different objects so that they can stay loosely coupled.
> Example: mediator  

## **1.1.5 Competing Qualities and Trade-offs**

***Satisfying Requirements***

> Some software design decisions will involve tradeoffs in different quality attributes, such as performance, convenience, and security.

***Functional Requirements***

> For software, there are functional requirements that describe what the system or application is expected to do.

***Non-Functional Requirements***

> There are also non-functional requirements that specify how well the system or application does what it does. Such requirements may describe how well the software runs in particular situations.

Other qualities to satisfy:

1. Reusability
2. Flexibility
3. Maintainability

Required qualities should be verified through techniques like **reviews** and **tests**  

Certain qualities can be validated with feedback from **end users**  

## **1.1.6 Record, Organize, and Refine Components**

Some requirements to identify when forming conceptual design

1. Components
2. Connections
3. Responsibilities

An important technique for representing information at a high level when forming the conceptual design  
**CRC cards** *(Class, Responsibility, Collaborator)*

CRC cards are used to:

1. Record,
2. organize, and
3. refine

components in design.

***CRC Card***

```
.----------------------------------.
|            Class Name            |
|----------------------------------|
| Responsibilities | Collaborators |
'------------------'---------------'
```

***Collaborators***

> Collaborators are other classes that the class interacts with to fulfill its responsibilities.

Therefore, the mapping is:

```
Components -> Class Name
Responsibilities -> Responsibilities
Connections -> Collaborators
```

***Example:***
Bank/ ATM machine

```
.-------------------------------------------.
|               Bank Customer               |
|------------------------.------------------|
| Responsibilities       | Collaborators    |
|   - Insert bank card   |   - Bank machine |
|   - Choose operation   |                  |
'------------------------'------------------'
```

```
.----------------------------------------------------.
|               Bank Machine                         |
|--------------------------------.-------------------|
| Responsibilities               | Collaborators     |
|   - Authenticate bank customer |   - Bank Customer |
|   - Display task options       |                   |
|   - Deposit and withdraw       |                   |
|   - Check balances             |                   |
'--------------------------------'-------------------'
```

```
.-------------------------------------------.
|                   Bank                    |
|------------------------.------------------|
|                        |                  |
'------------------------'------------------'
```

```
.-------------------------------------------.
|                  Network                  |
|------------------------.------------------|
|                        |                  |
'------------------------'------------------'
```

```
.-------------------------------------------.
|               Encryption                  |
|------------------------.------------------|
|                        |                  |
'------------------------'------------------'
```

and a few more, such as:

1. Card reader
2. Keypad
3. Display
4. Cheque slot
5. Cash dispenser
