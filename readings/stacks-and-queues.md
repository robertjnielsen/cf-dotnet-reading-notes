# Stacks And Queues

Stacks and Queues are data structures that consist of Nodes. Similar to a Linked List, they are managed by each Node holding a value, and a reference to another Node.

Let's take a look, shall we?!

## What Is A Stack?

Think of a stack like a vertical singly Linked List. It consists of Nodes, which each hold a value, and a reference to the next Node, but not the previous.

Stacks follow the FILO or LIFO concepts _(hint: they're the same thing)_ which means that the Last In is the First Out, or the First In is the Last Out.

Stacks also have a `Top` property, which works just like the `Head` property of a Linked List.

### Stack Methods

#### Push

`Push()` is an **O(1)** method that adds a new Node to the `Top` of the Stack.

```
static void Push(Node newNode)
{
    newNode.Next = Top;
    Top = newNode;
}
```

#### Pop

`Pop()` is an **O(1)** method that removes a Node from the `Top` of the Stack.

```
static Node Pop()
{
    Node tmp = Top;
    Top = Top.Next;
    tmp.Next = null;
    return tmp;
}
```

#### Peek

`Peek()` is an **O(1)** method that allows us to view the value of the `Top` Node in the Stack.

```
static int Peek()
{
    return Top.Value;
}
```

#### IsEmpty()

`IsEmpty()` is an **O(1)** method that returns a boolean value depending on whether or not the Stack contains any Node objects. True means that the Stack is empty.

```
static bool IsEmpty()
{
    return Top != null;
}
```
## What Is A Queue?

Queues are also similar to singly Linked Lists and Stacks, except that they follow the FIFO / LILO principles. This means that the First In is the First Out (or the Last In is the Last Out). Think of it by the name; a queue. A queue is a line of people waiting at the DMV, or to ride a roller coaster. The first person in line is the first to do the thing, and the last person in the line is the last to do the thing.

Queues have a `Front` property, which represents the first Node in the Queue, and a `Rear` property to represent the last Node in the Queue.

### Queue Methods

#### Enqueue

`Enqueue()` is an **O(1)** method that adds a Node to the `Rear` of the Queue.

```
static void Enqueue(Node newNode)
{
    Rear.Next = newNode;
    Rear = newNode;
}
```

#### Dequeue

`Dequeue()` is an **O(1)** method that removes a Node from the `Front` of the Queue.

```
public Node Dequeue()
{
    Node tmp = Front;
    Front = Front.Next;
    tmp.Next = null;
    return tmp;
}
```

#### Peek

`Peek()` is an **O(1)** method to view the value of the `Front` Node in the Queue.

```
public int Peek()
{
    return Front.Value;
}
```

#### IsEmpty

`IsEmpty()` is an **O(1)** method that returns a boolean value depending on whether or not the Queue contains any Node objects. True means that the Queue is empty. 

```
static bool IsEmpty()
{
    return Front != null;
}
```
