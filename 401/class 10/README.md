# Cheat Sheet: Stacks and Queues in C#
## Stacks:
**Definition:** A stack is a linear data structure that follows the Last In, First Out (LIFO) principle, where the last element added is the first one to be removed.

**Common operations:**

Push(item): Adds an item to the top of the stack.
Pop(): Removes and returns the top item from the stack.
Peek(): Returns the top item without removing it.
Count: Returns the number of items in the stack.
IsEmpty: Returns true if the stack is empty; otherwise, false.
Example in C#:

```
using System;
using System.Collections.Generic;

class Program
{
    static void Main(string[] args)
    {
        Stack<int> stack = new Stack<int>();

        stack.Push(10);
        stack.Push(20);
        stack.Push(30);

        Console.WriteLine("Top item: " + stack.Peek()); // Output: Top item: 30

        stack.Pop();
        Console.WriteLine("Top item after Pop(): " + stack.Peek()); // Output: Top item after Pop(): 20

        Console.WriteLine("Is the stack empty? " + (stack.Count == 0)); // Output: Is the stack empty? False
    }
}
```

## Queues:
**Definition:** A queue is a linear data structure that follows the First In, First Out (FIFO) principle, where the first element added is the first one to be removed.

**Common operations:**

Enqueue(item): Adds an item to the end of the queue.
Dequeue(): Removes and returns the first item from the queue.
Peek(): Returns the first item without removing it.
Count: Returns the number of items in the queue.
IsEmpty: Returns true if the queue is empty; otherwise, false.
Example in C#:

```
using System;
using System.Collections.Generic;

class Program
{
    static void Main(string[] args)
    {
        Queue<string> queue = new Queue<string>();

        queue.Enqueue("Alice");
        queue.Enqueue("Bob");
        queue.Enqueue("Carol");

        Console.WriteLine("First person: " + queue.Peek()); // Output: First person: Alice

        queue.Dequeue();
        Console.WriteLine("First person after Dequeue(): " + queue.Peek()); // Output: First person after Dequeue(): Bob

        Console.WriteLine("Is the queue empty? " + (queue.Count == 0)); // Output: Is the queue empty? False
    }
}
```
Remember that stacks and queues are essential data structures used in various algorithms and applications. Understanding their behavior and properties is crucial in solving programming problems efficiently.