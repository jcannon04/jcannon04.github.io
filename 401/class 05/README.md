# Linked List Cheatsheet

## Definition
```
public class LinkedListNode<T>
{
    public T Value { get; }
    public LinkedListNode<T> Next { get; set; }
    
    public LinkedListNode(T value)
    {
        Value = value;
    }
}

public class LinkedList<T>
{
    public LinkedListNode<T> Head { get; private set; }
    public LinkedListNode<T> Tail { get; private set; }
    public int Count { get; private set; }
    
    public LinkedList()
    {
        Head = null;
        Tail = null;
        Count = 0;
    }
}
```
## Operations

### AddFirst

#### Adds a new node with the specified value at the beginning of the linked list.
```
public void AddFirst(T value)
{
    LinkedListNode<T> newNode = new LinkedListNode<T>(value);
    
    if (Head == null)
    {
        Head = newNode;
        Tail = newNode;
    }
    else
    {
        newNode.Next = Head;
        Head = newNode;
    }
    
    Count++;
}
```
### AddLast

#### Adds a new node with the specified value at the end of the linked list.
```
public void AddLast(T value)
{
    LinkedListNode<T> newNode = new LinkedListNode<T>(value);
    
    if (Head == null)
    {
        Head = newNode;
        Tail = newNode;
    }
    else
    {
        Tail.Next = newNode;
        Tail = newNode;
    }
    
    Count++;
}
```

### RemoveFirst

#### Removes the first node from the linked list.
```
public void RemoveFirst()
{
    if (Head != null)
    {
        Head = Head.Next;
        
        if (Head == null)
        {
            Tail = null;
        }
        
        Count--;
    }
}
```

### RemoveLast

#### Removes the last node from the linked list.
```
public void RemoveLast()
{
    if (Head != null)
    {
        if (Head == Tail)
        {
            Head = null;
            Tail = null;
        }
        else
        {
            LinkedListNode<T> current = Head;
            
            while (current.Next != Tail)
            {
                current = current.Next;
            }
            
            current.Next = null;
            Tail = current;
        }
        
        Count--;
    }
}
```

### Contains

#### Checks if the linked list contains a node with the specified value.
```
public bool Contains(T value)
{
    LinkedListNode<T> current = Head;
    
    while (current != null)
    {
        if (EqualityComparer<T>.Default.Equals(current.Value, value))
        {
            return true;
        }
        
        current = current.Next;
    }
    
    return false;
}
```
### Clear

#### Removes all nodes from the linked list.
```
public void Clear()
{
    Head = null;
    Tail = null;
    Count = 0;
}
```

### Example Usage

```
LinkedList<int> linkedList = new LinkedList<int>();

linkedList.AddLast(10);
linkedList.AddLast(20);
linkedList.AddLast(30);
linkedList.AddFirst(5);

linkedList.RemoveLast();
linkedList.RemoveFirst();

bool contains20 = linkedList.Contains(20);
int count = linkedList.Count;

linkedList.Clear();
```

This cheatsheet provides a quick reference for common operations on a linked list in C#. You can use the provided code snippets and example usage to work with linked lists in your C# programs.