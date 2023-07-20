# Collections Cheat Sheet
## Common Collections in C#
* List<T>: A dynamic-sized list that can hold elements of a specific type.
* Dictionary<TKey, TValue>: A collection of key-value pairs, where each key must be unique.
* Queue<T>: A first-in, first-out (FIFO) collection of elements.
* Stack<T>: A last-in, first-out (LIFO) collection of elements.
* HashSet<T>: A set of unique elements with no specific order.
* LinkedList<T>: A doubly-linked list of elements.
* SortedDictionary<TKey, TValue>: A dictionary with keys sorted in their natural order.
* SortedList<TKey, TValue>: A list of key-value pairs sorted by key.
* ConcurrentDictionary<TKey, TValue>: A thread-safe dictionary for concurrent access.
* ConcurrentQueue<T>: A thread-safe FIFO queue.
* ConcurrentStack<T>: A thread-safe LIFO stack.
* BlockingCollection<T>: A thread-safe collection for producer-consumer patterns.

# Enum Cheat Sheet

## Defining an Enum

```
enum Season
{
    Spring,
    Summer,
    Autumn,
    Winter
}
```
## Enum Members and Associated Values

```
enum ErrorCode : ushort
{
    None = 0,
    Unknown = 1,
    ConnectionLost = 100,
    OutlierReading = 200
}
```
## Enum with Bit Flags

```
[Flags]
enum Days
{
    None = 0b_0000_0000,  // 0
    Monday = 0b_0000_0001,  // 1
    Tuesday = 0b_0000_0010,  // 2
    // Add more members as powers of two (for bit flags)
}
```
## Enum Operations

```
Season currentSeason = Season.Spring;

// Conversions
int numericValue = (int)currentSeason; // Convert enum to int
Season convertedSeason = (Season)numericValue; // Convert int to enum

// Check if enum contains a member with a specific value
bool isAutumn = Enum.IsDefined(typeof(Season), 2); // Checks if Autumn (value 2) exists

// Bitwise operations for enums with bit flags
Days meetingDays = Days.Monday | Days.Wednesday | Days.Friday;
Days workingFromHomeDays = Days.Thursday | Days.Friday;
Days commonDays = meetingDays & workingFromHomeDays;
bool hasTuesdayMeeting = (meetingDays & Days.Tuesday) == Days.Tuesday;
Note: The [Flags] attribute is used to declare enums as bit flags to combine multiple choices.
```

Remember to include appropriate using directives for the collections you use, such as using System.Collections.Generic; for List<T> and Dictionary<TKey, TValue>, using System.Collections.Concurrent; for concurrent collections, etc.

This cheat sheet provides a quick reference to the most commonly used collections and enums in C#. You can use these data structures to efficiently manage and represent data in your applications.