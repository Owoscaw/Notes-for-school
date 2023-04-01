
## ADTs:

Data types consist of 3 archetypes, Elementary, Composite, and Abstract. An elementary data type is a simple data type used in all programming languages, such as an integer, character, or Boolean. A composite data type is the combination of multiple elementary data types, such as a string or an array. An abstract data type is a logical description of how we view the data and possible operations, an example would be a list or a queue. 

In an ADT (Abstract Data Type), the focus is on data representation as opposed to constructions. An encapsulation is created around the data, hiding information. Efficiency is always lost in abstraction. ADTs are often useful in [[Network topologies]] and representing [[Graph theory|graphs]].

## Queue:

In a queue, elements can only join the queue at the back and leave at the front. Things cannot be inserted in positions other than the back. There are 4 distinct operations that can be performed on a queue; add to back of queue, remove from front of queue, check if empty queue, check if full queue. Pointers can be used in an array in order to indicate the front and back of the queue, this solves the problem of having to shift every element down by one every time an element is removed. Because you cannot remove from an empty queue or add to a full queue, the maximum size of the queue must be specified when the queue is initialised. A variable, size, may also be needed in order to specify the current size of the queue.

\>enQueue(item) - adds item to back of queue

\>deQueue() - removes and returns item from the front

\>isEmpty() - indicates if the queue is empty

\>isFull() - indicates if the queue if full

A problem can arise when the pointers for the start and the end are at the same place, in which scenario the queue would be empty and full at the same time. A circular queue overcomes this problem by reusing spaces that have been freed by dequeuing from the front of the array. The MOD function can be used to implement this, as the position of an object being added wraps around the "end" of the queue to find a new position, that position being the result from the MOD operation being applied to an index with the size of the queue. 

In a priority queue, items are allowed to jump the queue to the front. This implementation is used when items being queued have an associated priority. In the example of the buses, buses ending with an A could be high priority, B could be medium, C could be low e.c.t. 

Static data structures have a fixed size, they cannot grow or shrink. Dynamic data structures can grow and shrinks, memory is allocated and deallocated from a dedicated heap. Excessive allocation of memory can cause overflow.



Pseudocode:

q = array of maxSize elements
front = 0
rear = -1
size = 0

DEFINE SUBROUTINE isFull()
	IF size == maxSize DO
		RETURN TRUE
	ELSE DO
		RETURN FALSE
	END IF
END DEFINE


DEFINE SUBROUTINE isEmpty()
	IF size == 0 DO
		RETURN TRUE
	ELSE DO 
		RETURN FALSE
	END IF
END DEFINE

DEFINE SUBROUTINE enQueue(item)
	IF NOT(isFull()) DO
		rear = (rear+1)%maxSize
		q[rear] = item
		size += 1
	ELSE DO
		RETURN
	END IF
END DEFINE

DEFINE SUBROUTINE deQueue()
	IF NOT(isEmpty()) DO
		popped = q[front]
		front = (front+1)%maxSize
		size -= 1
		RETURN popped
	ELSE DO
		RETURN
	END IF
END DEFINE
