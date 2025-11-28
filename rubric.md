# Project Assessment Rubric

**Project:** StudyZone - Data Structures Implementation
**Section:** C2A
**Course:** Object Oriented Programming

## Grading Breakdown

### 1. Class Diagram Completeness (25%)
**Score:** 3/5
**Notes:** UML diagram provided via Figma (uml.png). The diagram shows a hierarchical component structure with multiple classes and their methods, demonstrating the Study Timer system architecture. However, the diagram lacks proper UML notation - classes are not presented in standard UML format with clear separation of attributes and methods, and relationships between classes are shown as simple flowchart-style connections rather than proper UML associations/compositions with cardinalities. The diagram provides a basic overview but is incomplete from a formal UML perspective.

### 2. Java Program - OOP Concepts (50%)
**Score:** 2/5
**Notes:**
- **Encapsulation (Present):** Inner static classes (MyArrayList, MyLinkedList, MyStack, MyQueue, BST) encapsulate their data structures with private/package fields (arr, size, head, top, front, rear, root). Methods provide controlled access to these structures.
- **Abstraction (Limited):** While the code uses nested Node classes to abstract data structure internals, there are no abstract classes or interfaces defining common behavior across data structures. Each structure is implemented independently without a unifying abstraction.
- **Inheritance (Minimal):** The Node inner classes demonstrate basic inheritance concepts (e.g., BST.Node and MyLinkedList.Node), but there's no class hierarchy for the data structures themselves. All structures are defined as independent static inner classes within Main.
- **Polymorphism (Missing):** No method overriding, interface implementations, or polymorphic behavior demonstrated. Each data structure operates independently without shared interfaces or base classes.

The project demonstrates basic encapsulation through data hiding but lacks advanced OOP concepts like inheritance hierarchies, abstract classes, or polymorphic behavior. The code is more procedural in nature, focusing on data structures rather than object-oriented design patterns. This appears to be more of a Data Structures project than an OOP project.

### 3. Git Usage & Collaboration (15%)
**Score:** 2/5
**Notes:** Minimal collaboration with only 4 total commits from 2 contributors: richardlorenzperez-cpu (3 commits) and Michael Ong (1 commit). The very low commit count suggests limited use of version control, possibly with most work done in a single session or offline. This indicates minimal collaborative development or git workflow practices.

### 4. Base Grade (10%)
**Score:** 5/5

### 5. Extra Points (up to 6)

**Features:** 1/5
- Console basic

**Code Quality:** 0.5/1.0
- Variable naming: 0.25/0.5
- Code organization: 0.25/0.5

**Extra Points Total:** +1.5

---

## Final Grade: 60 + 1.5 = **61.5/100**

*Assessment generated based on project analysis.*
