# Linked lists

## Reverse a linked list.
*Write a function that takes the first Node in a linked list, reverse it, and returns the first Node in the resulting linked list.*

**Solution**

To accomplish this, we maintain references to three consecutive nodes in the linked list, reverse, first, and second.
At each iteration we extract the node first from the original linked list and insert it at the beginning of the reversed list.
We maintain the invariant that first is the first node of what's left of the original list,
second is the second node of what's left of the original list, and reverse is the first node of the resulting reversed list.

```java
    public static Node reverse(Node list) {
       if (first == null || first.next == null) return first;
       Node first   = list;
       Node reverse = null;
       while (first != null) {
          Node second = first.next;
          first.next  = reverse;
          reverse     = first;
          first       = second;
       }
       return reverse;
    }
```

## Reverse a Linked List in groups of given size
*Given a linked list, write a function to reverse every k nodes (where k is an input to the function). *

Example:
Inputs:  1->2->3->4->5->6->7->8->NULL and k = 3
Output:  3->2->1->6->5->4->8->7->NULL.

Inputs:   1->2->3->4->5->6->7->8->NULL and k = 5
Output:  5->4->3->2->1->8->7->6->NULL.

**Solution**

## Mth-to-Last Element of a Singly Linked List

http://www.geeksforgeeks.org/reverse-a-list-in-groups-of-given-size/

TODO

**Solution**
	
	1) calculate size (n) of list - traverse, storing each node, checking is this end, if not use node's NEXT pointer 
	2) element = n - m - traverse
	
## Check for loop in linked list

**Solution**
Start slow pointer at the head of the list
Start fast pointer at second node
Loop infinitely

If the fast pointer reaches a null pointer
Return that the list is null terminated
If the fast pointer moves onto or over the slow pointer
Return that there is a cycle
Advance the slow pointer one node
Advance the fast pointer two nodes

## Find start node of loop in linked list
TODO

http://www.java2blog.com/2016/02/find-start-node-of-loop-in-linkedlist.html

## Check if the linked list is palindrome

**Solution**
 1   Find middle element of linked list using slow and fast pointer method .
 2   Reverse second part of linked list
 3   Compare first and second part of linked list if it matches then linked list is palindrome.

http://www.java2blog.com/2016/04/how-to-check-if-linked-list-is.html

## Rotate linked list

## Implement merge sort on lists

## Merge Sort for Doubly Linked List
Similar to singly linked (only maintain prev poniter).
http://www.geeksforgeeks.org/merge-sort-for-doubly-linked-list/

## Merge two sorted lists using O(1) space

## Find intersection of two sorted lists

TODO

## Add two numbers represented by linked lists

TODO

http://www.geeksforgeeks.org/sum-of-two-linked-lists/


## Delete a node having this element in singly linked

Move data & next pointer from next node to the one which should be deleted

## Delete n nodes after m node of singly linked list

TODO

## Detect and remove loop in singly linked list

TODO

## Remove duplicates in unsorted list

http://www.geeksforgeeks.org/remove-duplicates-from-an-unsorted-linked-list/

1) two loops (n^2)
2) merge sort fist, then traverse and remove dups nlogn
3) use hash table put, remove dups - n (linear assuming hash is O(1))