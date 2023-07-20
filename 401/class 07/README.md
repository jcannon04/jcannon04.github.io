# Class 07 Interfaces

An interface contains definitions for a group of related functionalities that a non-abstract class or struct must implement. It can define static methods that must have an implementation but cannot declare instance data such as fields

**Problem Interfaces Solve:**

Interfaces are designed to separate how an object is used from how it is implemented. This allows code to work with different implementations of a set of responsibilities without explicitly handling each one.

**Interfaces as Contracts:**
Interfaces specify expectations that classes implementing them must fulfill. They ensure that classes supporting an interface will have all the methods defined in the interface.

**Difference from Concrete Inheritance:** 

Interfaces are different from concrete inheritance. While concrete inheritance states that a class "is" another class, an interface states that a class "implements" the interface.

**Always Implemented by More than One Class:**

Interfaces are typically used to solve a problem where multiple classes implement the same contract. If only one class currently implements an interface, it might be an indication of incorrect usage.

**Example:**

```
interface IEquatable<T>
{
    bool Equals(T obj);
}

public class Car : IEquatable<Car>
{
    // Properties
    public string? Make { get; set; }
    public string? Model { get; set; }
    public string? Year { get; set; }

    // Implementation of IEquatable<T> interface
    public bool Equals(Car? car)
    {
        return (this.Make, this.Model, this.Year) ==
            (car?.Make, car?.Model, car?.Year);
    }
}

```

Interfaces provide a powerful mechanism to define contracts that classes or structs must adhere to, allowing for flexible and efficient code design.

