This chapter lays the groundwork for understanding **object-oriented (OO) concepts**, emphasizing that they are fundamental to OO development, more so than specific technologies. The focus is on the **"why"** behind OO, not just the "how."

### 🕰️ A Brief History of OO

- OO development has roots in the early 1960s, but it gained traction in the **mid-to-late 1990s**.
- The rise of OO methodologies coincided with the emergence of the **Internet** as a business and entertainment platform, because objects are well suited for networks.
- **Object-oriented technologies** were well positioned to develop new web-based technologies.
- While **technologies change rapidly**, OO _concepts evolve_ and remain relevant.
- These core concepts are as important today as they were 25 years ago.

### 🎯 Fundamental OO Concepts

The core of OO is based on a few key ideas:

- **Encapsulation**: Combining data (attributes) and behaviors (methods) into a single object.
- **Inheritance**: Allowing a class to inherit attributes and methods from another class, promoting code reuse and hierarchy.
- **Polymorphism**: Allowing objects of different classes to respond to the same message in their own way.
- **Composition**: Building objects by combining other objects.

These concepts form the basis for designing object-oriented systems. The book emphasizes understanding these core concepts even if you choose to avoid some of them, like inheritance, in your designs. These concepts are constantly being reinterpreted.

### 🤝 Objects and Legacy Systems

- As OO became mainstream, a key issue was integrating it with **existing (legacy) systems**.
- OO and structured programming **are complementary**; objects integrate well with structured code, which is not meant to be replaced.
- Many older, non-OO legacy systems still work well and should not be changed just for the sake of change.
- New development should consider using **OO technologies**, and legacy systems can be wrapped in object wrappers.
- Object wrappers are **object-oriented code** that includes other code inside.

### 🌐 The Rise of the Mobile Web

- The Internet's emergence significantly drove the shift to OO technologies, because **objects are well-suited for networks**.
- Mobile networks have now become a major factor, so the term **"mobile web"** encompasses both mobile app and web development.
- Businesses are moving towards object based technologies in **electronic commerce**.

### 🆚 Procedural vs. OO Programming

- An **object** is defined by both its attributes and its behaviors, and both are contained within the object.
- In **procedural programming**, data is separate from the procedures that act on it.
- In **OO design**, attributes and behaviors are contained within a single object.
- Data is often **global** in procedural programming, leading to uncontrolled and unpredictable access, making testing and debugging harder.
- **OO** addresses these problems by combining data and behavior into complete packages with controlled access.
- With proper design, there is no such thing as global data in an OO model, providing **data integrity**.
- Objects are more than just data structures; they also contain methods that act on data, with controlled access to members.

### 📦 Encapsulation and Data Hiding

- **Data hiding** restricts access to certain attributes and methods, while **encapsulation** combines attributes and methods.
- Objects communicate by sending **messages** to each other, which are calls to an object's methods.
- Objects should not manipulate the internal data of other objects.
- It is better to build small objects with specific tasks rather than large objects that perform many.

### 📡 Data Transmission in Procedural vs. OO

- **Procedural programming** transmits only the necessary data across a network, expecting the other end to know how to use it.
- **OO programming** transmits entire objects, including both data and the operations to manipulate that data.

### 🧱 What Exactly Is an Object?

- Objects are the **building blocks of an OO program**.
- Objects contain:
    - **Attributes**: Data that describes the state of the object.
    - **Methods**: Behaviors that define what an object can do.
- **Getter and setter** methods provide controlled access to the attributes, supporting data hiding.
- An object communicates with other objects by calling their methods.

### 📜 Classes: Blueprints for Objects

- A **class** is a blueprint or template for creating objects, defining attributes and behaviors of the object.
- Objects are **instances** of a class.
- Each object has its own copy of attributes but typically points to the same implementation of methods.
- Classes define attributes and behaviors that all objects created with that class will possess.
- Classes are pieces of code from which objects are instantiated and can be distributed individually or as part of a library.
- You must **design a class** before creating an object.

### 🛠️ Essential Class Concepts

- **Attributes** store the state of each object.
- **Methods** implement class behaviors.
- Access designations (public, private, protected) control visibility and access.
- **Messages** are how objects communicate by invoking each other's methods.

### 🖼️ UML Class Diagrams

- **UML class diagrams** are used to visualize classes and their relationships.
- Class diagrams consist of three sections: name, attributes, and methods.

### 🔒 Encapsulation and Data Hiding

- Objects should reveal only the **interfaces** needed for interaction and hide non-essential details.
- **Encapsulation** combines attributes and behaviors, while **data hiding** controls access.
- Interfaces define the means of communication between objects, and the implementation includes anything defined as private.
- All attributes should be declared as **private** to ensure proper data hiding.
- **Getters and setters** provide controlled access to the attributes.

### 🔌 Interface vs. Implementation

- The **interface** defines how users interact with a class, often with public methods.
- The **implementation** is the internal workings of the class, hidden from the user.
- A real-world example is the relationship of a toaster, an electrical outlet, and the power company.

### 🧬 Inheritance

- **Inheritance** allows a class to inherit attributes and methods of another class.
- It promotes code reuse and the organization of classes into hierarchies.
- **Superclasses** (parent or base classes) contain common attributes and behaviors, while **subclasses** (child or derived classes) extend the superclass.
- When an object is instantiated, it contains everything in its own class as well as everything in its parent class.
- Behaviors are often described in interfaces while direct inheritance is most often used for inheriting attributes.
- Inheritance can create multiple levels of abstraction, making it complex, but it can provide a great deal of design flexibility.
- Most OO languages use **single inheritance** (one parent), but some languages, like C++, allow **multiple inheritance** (multiple parents).

### ↔️ Is-a Relationships

- An **is-a relationship** indicates that a subclass is a type of its superclass (e.g., a circle is a shape).
- Subclasses can do anything the superclass can do.

### 🎭 Polymorphism

- **Polymorphism** allows objects of different classes to respond differently to the same message.
- Subclasses inherit interfaces from their superclass, but can provide their own response to messages.
- **Overriding** means replacing a parent's implementation with a child's implementation.
- For example, different shapes can respond differently to a "draw" method.
- **Abstract methods** in a superclass require the subclasses to provide a specific implementation.
- **Constructors** are special methods used to create and initialize objects.
- Polymorphism provides standardization for interfaces across classes, as well as applications.

### 🧩 Composition

- **Composition** is building objects from other objects (e.g., a car has-a engine).
- **Has-a relationships** are used to describe composition (versus the is-a relationship of inheritance).
- Composition offers another way to achieve abstraction.

### 🔑 Key Concepts from Chapter 1

- **Encapsulation**: Combining data and behavior into a single object.
- **Inheritance**: Creating new classes by inheriting from existing ones.
- **Polymorphism**: Allowing similar objects to respond differently to the same message.
- **Composition**: Building objects from other objects.

This chapter has provided the fundamental OO concepts, providing a solid foundation for the rest of the book.