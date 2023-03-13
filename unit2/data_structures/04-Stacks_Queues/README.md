
# Stacks and Queues

- [Stacks and Queues](#stacks-and-queues)
  - [Stacks](#stacks)
    - [Stack Array Implementation](#stack-array-implementation)
    - [Stack LinkedList Implementation](#stack-linkedlist-implementation)
  - [Queues](#queues)
    - [Queue Array Implementation](#queue-array-implementation)
    - [Queue LinkedList Implementation](#queue-linkedlist-implementation)
  - [Big O](#big-o)

![stacks and queues](assets/stackqueue.png)

## Stacks

FILO - "first in last out" data structure. Think of a stack of papers. 

### Stack Array Implementation

```javascript
class Stack {
 
    constructor() {
        this.items = [];
    }
 
    push(element) {
        this.items.push(element);
    }
    
    pop() {
        return this.items.pop();
    }
}
```

### Stack LinkedList Implementation

```javascript
class Stack {

  constructor() {
    this.head = null;
    this.length = 0;
  }

  push(val) {
    let newNode = new Node(val);
    if (!this.head) {
      this.head = newNode;
    }
    else {
      let temp = this.head;
      this.head = newNode;
      this.head.next = temp;
    }
    this.length++;
  }

  pop() {
    // your code
  }
}
```

## Queues

FIFO - "First in first out". Think of a line or queue of people waiting for a movie.

![queue](assets/queue.png)

### Queue Array Implementation
```javascript
class Queue {
 
    constructor() {
        this.items = [];
    }
 
    enqueue(element) {
        this.items.push(element);
    }
    
    dequeue() {
        return this.items.shift();
    }
}
```

### Queue LinkedList Implementation
  
```javascript
class Queue {

  constructor() {
    this.head = null;
    this.tail = null;
    this.length = 0;
  }

  enqueue(val) {
    let newNode = new Node(val);
    if (!this.head) {
      this.head = newNode;
      this.tail = newNode;
    }
    else {
      this.tail.next = newNode;
      this.tail = newNode;
    }
    
    this.length++;
  }

  dequeue() {
    // your code
  }
}
```

## Big O
  
| Data Structure |  Add |      Remove     |
|:--------------:|:----:|:---------------:|
| Stack - Array  | O(1) |       O(1)      |
| Stack - LL     | O(1) |       O(1)      |
| Queue - Array  | O(1) |       O(N)      |
| Queue - LL     | O(1) |       O(1)      |