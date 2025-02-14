TestIterator.java :

TODO Question: What happens if you use list.remove(Integer.valueOf(77))?
ANSWER: Doing so will throw a ConcurrentModificationException, since this directly calls remove(Object o) on the list,
        modifying the collection while an iterator is actively iterating over it.

TestList.java:

TODO Question: Also try with a LinkedList - does it make any difference?
ANSWER: In terms of test behavior, there is no difference. However, because both are different data structures,
        some differences will be noted, such as insertion/deletion time complexity, which tends to be faster on
        LinkedList than on ArrayList.

TODO Question: What does this method do? (list.remove(5);

ANSWER: This method removes the element at index 5 (not the value 5 itself).

TODO Question: What does this one do? (list.remove(Integer.valueOf(5));)

ANSWER: This method removes the first occurrence of the value 5 from the list if it exists.


PERFORMANCE TEST:

LinkedList Add/Remove Time: 118.722672 ms
ArrayList Add/Remove Time: 194.642078 ms
LinkedList Access Time: 37.983289 ms
ArrayList Access Time: 12.641071 ms

TODO Question: What conclusions can you draw about the performance of LinkedList vs. ArrayList when
               comparing their running times for AddRemove vs. Access? Record those running times in README.txt!

           1. Linked List tend to perform better at adding and deleting elements, this is observable through the time
              it takes to complete these operations. While arrayList tend to take longer to complete these operations
              the time increase as the sizes increase.
              However, for operations that require addRemove/Access, ArrayList tend to perform better than LinkedList,
              this is also observable through the time it takes to complete these operations above. Furthermore, it's
              well-know that the time complexity for these operation is O(N) for Linklist while for arrays and
              ArrayList it's O(1).
