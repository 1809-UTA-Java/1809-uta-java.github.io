# Data Structures in Java  
Java provides the **Collection** interface which provides a framework for several diffrent containers which will be disscussed below. All interfaces share **Collection** as their superinterface.  
  
## List  
A **List** is an ordered collection of elements. A user has the ability to place an element anywhere in the list. The elements are accessable by their index. Unlike **Set**, **List** typically allows for duplicate elements such that element1.equals(element2). In addition to duplicates, **List** allow for multiple null elemts to be stored.  
  
## Set  
**Set** is a collection of non duplicate elements meaning there will never exist a situation where element1.equals(element2). In addition to this, it is implied that there can only exist one null element due to the no duplicates rule.  
  
## Queue  
**Queue** is a collection of elements who in essence cannot be iterated, instead the **Queue** follows the **FIFO** (First In First Out) rule. When an element is added to the **Queue** it is placed at the back and when an element is pulled it is pulled from the from the front (index :0).  
  
## Deque
**Deque** extends **Queue** but augments the ability to insert and remove elements at either end. The name is short for "Double Ended Queue" and is pronounced "Deck".  
  
### Children of List, Set, Queue, and Deque  
  
## ArrayList  
An **ArrayList** extends **AbstractList** and implements **List** (among others). **ArrayList** provides a dynamic array implementation. **ArrayList** has a dynimic capacity which is resized when the user fills the container. At all times the **ArrayList** capacity will be either larger or the same size as the number of elements it contians.  
  
## HashSet  
**HashSet** extends **AbstractSet** and implements **Set** (among others). **HashSet** implements the **Set** interface which organizes elemts based on a hash table. Due to the hash table, there is no guananteed order of iteration.  
  
## TreeSet  
**TreeSet** extends **AbstractSet** and implements **NavigableSet** (!!!!!). Elements in the set are ordered using natural ordering (sorted and ascending order). **TreeSet** does not preserve the insertion order of elements but elements are sorted by keys. **TreeSet** is essentially an implementation of a self-balancing binary search tree.  
  
  
