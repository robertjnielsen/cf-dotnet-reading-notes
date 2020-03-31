# Linked Lists

## What Are Linked Lists?

Of the many ways to store data (known as **_data structures_**), one is called a **Linked List**.

A linked list are a type of data structure known as a **linear data structure**. They're linear because they are constructed and traversed in a sequence, as opposed to **non-linear data structures** which do not have to be arranged in a sequential structure.

## Memory Management

When a typical linear data structure, such as an array is declared, it needs to know how much memory to allocate for that array. All of the memory for that array would have to be allocated in one contiguous block. These types of data structures are known as **static data structures**.

When a linked list of the same size is declared, it still needs the same amount of memory allocated, but that memory does not need to be contiguous. It can be scattered around in any free blocks that it can find. It is this quality that defines link lists as a type of data structure known as **dynamic data structures**.

But how does this work? How can we store the different pieces of a linked list in various locations in memory?

Well...

## Nodes

Linked lists are made of chunks of data known as **nodes**. The nodes are the elements of the list.

The first node in a linked list is referred to as the **head**, and is the starting point for the list.

The last node in a linked list isn't a typical node, but rather a node that points to **null**. This denotes the end of the list.

Each node has to parts to it: the **data**, which is the information that the node contains, and a reference to the next node in the list known as the **Next** value.

A single node may not know how long the list is, or even where in the list it "lives". All it needs to know is the value it holds, and the address to the next node in the sequence.

Because of this, linked lists can be allocated in memory dynamically. Once you access the head node, it holds a reference to the next node, and so on, always pointing to the location in memory of the next value you are seeking.
