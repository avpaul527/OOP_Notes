# Object Oriented Programming
*Object Oriented Notes from HeadFirst Java Ch. 9 &amp; Pluralsight 8-10*

## HeadFirst Java: Chapter 9 - Life and Death of an Object
- 2 areas of Memory
  - Heap - where all objects live
  - Stack - where method invocations and local variables live
  - *if local variable is a reference to and object, only the variable(reference) goes on the stack
- Objects are created using the **new** keyword, followed by the constructor.
- Constructors are called to initialize an object.
  - Constructor -invoked when an object is instantiated.
  - Constructors can have parameters to initialize object properties.
  - If you have multiple constructors (overloaded), they must have different argument lists.
  - Overloaded - more than one constructor in a class.
- Default values -0/0.0/false for primitives and null for references.
- Default constructor are always no-arg
- Abstract classes do not use **new**
- Abstact class constructor runs when an instance of concrete subclass is made from it.
- To call a super constructor you must use **super()**
- Superclass = Parent class  |  Subclass = Child class
- Superclass must be complete before constructing the subclass.
- Constructor can have a call to super() OR this(), but never both
- Use this() to call a constructor from overloaded constructor in the same class
- this() can be used only in a constructor and must be the first statement in a 
constructor
- Java uses automatic garbage collection (memory management)
- Referencing **null** = empty instance of an object
- If you use the dot operator on a null reference, you will get a NullPointerException at runtime.

## Pluralsight 8-10 Notes
 ### Classes and Objects
 - Objects encapsulate data, operations, and usage semantics.
 - Allow storage and manipulation details to be hidden.
 - Class is a template for creating objects
 - Java source file name is same as class
 - Class is made up of state and executable code (Fields, Methods, Constructors)
 - new keyword -create a class instance (object)
 - Encapsulation - implementation details of a class are generally hidden (achieved with access modifiers
 - No access modifier - only visible within its own package
 - public - visible everywhere
 - private - only visible within the declaring class
 - this - reference to current object that allows it to pass itself as parameter
 - null - uncreated object (can be assigned to any reference variable)
 - Use methods to control field access
 - Accessor/Mutator pattern
    - accessor retrieves field value(getter)
    - mutator modifies field value(setter)

### Implementing Class Constructors and Initializers
- Class initial state (3 ways to establish)
  - Field initializers (can be an equation, can include other fields, can include method calls)
  - Constructors (code that runs during object creation, same name as class, no return type, can be non-public)
    - Chaining constructors - one constructor can call another   
  - Initialization blocks (share code across all constructors, cannot receive parameters, a class can have multiple)
- Initialization & construction order: field initializers, initialization blocks, constructors.

### Using Static Members
- Static Members are shared class-wide, not associated with individual instance (declared using static keyword)
- Static Members can be fields and methods
- Static import statement (used with static methods, and allows method name to be used without being class-qualified)
- Static initialization blocks perform one-time type initialization.
  - has access to static members only
  - execute before type's first use
  - Statements enclosed in bracket are preceded with static keyword & code is outside of any method or constructor
  
