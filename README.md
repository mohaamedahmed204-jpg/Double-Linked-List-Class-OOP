# Double-Linked-List-Class-OOP

A robust, reusable, and header-only **Doubly Linked List** library implemented in **C++** utilizing Object-Oriented Programming (OOP) principles and C++ Templates. 

This library is designed for high performance, clean memory management, and ease of integration into any C++ project, supporting generic data types.

---

## 🚀 Features

* **Template-Based (`class T`)**: Works with any data type (integers, strings, custom objects, etc.).
* **Object-Oriented Design**: Encapsulated cleanly inside a dedicated class structure (`clsDblLinkedList`).
* **$O(1)$ Size Tracking**: Uses an inline static/tracked tracking mechanism to retrieve the list size instantly without traversal.
* **Comprehensive Operations**: Supports insertion, deletion, searching, updating, indexing, traversal, and reversal.
* **Safe Memory Management**: Proper pointer handling and node destruction to prevent memory leaks.

---

## 📂 Class Architecture & Methods

Here is an overview of the core public interface provided by `clsDblLinkedList<T>`:

### 1. Element Access & Information
* `T Size()`: Returns the total number of nodes in the list in $O(1)$ time.
* `bool IsEmpty()`: Checks if the list contains any elements.
* `Node* Find(T Value)`: Searches for a specific value and returns a pointer to its node (or `nullptr` if not found).
* `Node* GetNode(unsigned int Order)`: Retrieves a node by its zero-based index.
* `T GetItem(unsigned int Order)`: Returns the value stored at a specific index.

### 2. Insertion Operations
* `void InsertAtBeginning(T value)`: Adds a new node at the head of the list.
* `void InsertAtEnd(T value)`: Appends a new node to the tail of the list.
* `void InsertAfter(Node* current, T value)`: Inserts a new node directly after a specified node pointer.
* `void InsertAfter(unsigned int Order, T value)`: Inserts a new node after a specified index order.

### 3. Deletion Operations
* `void DeleteFirstNode()`: Removes the head node and frees memory.
* `void DeleteLastNode()`: Removes the tail node and frees memory.
* `void DeleteNode(Node*& NodeToDelete)`: Safely unlinks and deletes an arbitrary node pointer.
* `void Clear()`: Deallocates the entire list, resetting it to an empty state.

### 4. Utilities & Manipulation
* `void PrintList()`: Traverses and prints all elements sequentially.
* `void Reverse()`: Reverses the entire doubly linked list in-place.
* `void UpdateItem(unsigned int Order, T Value)`: Updates the value of an item at a specific index.

---

## 💻 Code Example

Here is a quick example of how to initialize and use the library:

```cpp
#include <iostream>
#include "clsDblLinkedList.h"

using namespace std;

int main() {
    clsDblLinkedList<int> numbersList;

    // Insert elements
    numbersList.InsertAtEnd(10);
    numbersList.InsertAtEnd(20);
    numbersList.InsertAtBeginning(5);

    // Print list
    cout << "List elements: ";
    numbersList.PrintList(); // Output: 5 10 20

    // Check size
    cout << "Size: " << numbersList.Size() << endl; // Output: 3

    // Update item
    numbersList.UpdateItem(1, 99); // Updates index 1 to 99
    
    cout << "After update: ";
    numbersList.PrintList(); // Output: 5 99 20

    return 0;
}
```
## 🧑‍🏫 Course Information



Platform: ProgrammingAdvices

Website: https://programmingadvices.com

Instructor: Dr. Mohammed Abu-Hadhoud

Course: 13 - Algorithms & Problem Solving – Level 5

## 👤 Author

Mohamed Ahmed Gwiada 
GitHub: @mohaamedahmed204-jpg
