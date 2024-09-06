**Skip List**

Skip List is a data structure that allows fast search within an ordered sequence of elements. The search is made fast by maintaining a linked hierarchy of subsequences, with each successive subsequence skipping over fewer elements than the previous one. It allows quick search, insertions and deletions of elements.

**Description**
- The elements used for a skip list can contain more than one pointer since they can participate in more than one list.
- Insertions [add (x)] and deletions [remove (x)] are implemented much like the corresponding linked-list operations, except that tall elements must be inserted into or deleted from more than one linked list.
- Before adding a node to a skip list, we need to find [find (x)] the position where the node needs to be added.
- Inserting a particular node is done in a random order [(randomLevel (level)] to make the search efficient. Levels are maintained and we can directly reach a particular level when we are finding [findIndex (n)] an element.
- The list is rebuilt using the rebuild() function to make it a perfect skip list. Rebuilding made the skip list much faster.
- I compared the skip list implementation with the tree map and evaluated their performance.
- Since we need to compare only for add, remove and contains functions, I have created seepage files (TreeMapComparison.java and SkipListComparison.java) which implements only the above mentioned functions.

**Inference**
- SkipList performs better than TreeMap after SkipList was rebuilt. However, without rebuild, both the data structures are performing more or less the same.

**Methods implemented**
1. add (x) — Add an element x to the list.
2. find (x) — Before insertion / deletion, this method will find the position of the given element.
3. randomLevel (level) — Method to randomly generate a level where new nodes can be placed.
4. ceiling (x) — Finds the least element that is greater than or equal to the number x.
5. floor (x) — Finds the greatest element that is less than or equal to the number x.
6. contains (x) — Checks whether the list contains the element x.
7. findIndex (n) — Finds the element present in the given index.
8. first () — Finds the first element of the list.
9. last () — Finds the last element in the list.
10. isEmpty () — Checks whether the list is empty or not.
11. iterator () — Method to iterate over the skip list.
12. rebuild () — Used to rebuild a list to a perfect skip list.
13. remove (x) — Removes the element x from the skip list.
14. size () — Displays the number of elements in the list.

**Results**
Input 1 - Running Time : 17 ms
Input 2 - Running Time : 760 ms 
Input 3 - Running Time : 5321 sec
