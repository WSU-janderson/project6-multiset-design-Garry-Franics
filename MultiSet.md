# MultiSet Design
## Introduction

This document details the design of my MultiSet ADT. A MultiSet is a collection of elements in which elements are able
to be repeated. My design is for a video game inventory that stores string item names and size_t counts. It will
be built on a AVLTree<string, size_t>.

## Design Philosophy

My MultiSet prioritizes simplicity as the main quality of its design. I want this ADT to be easy to implement and modify
if needed. Game inventories have all kinds of different specifications. Some have weight limits or a fixed maximum
number of items, others let you carry as many things as you want with no limitations at all. Because games have all of
these variations, I want my MultiSet to be as simplistic as possible so it can be used as a base for any system. Because
of this there will be no restrictions on how many key pairs the MultiSet can store.

## Core Operations
### Insert

The `Insert` operation will take a key and a value then attempt to add the pair to the MultiSet's AVLTree. The key will
be the name of the item that is being added to the player's inventory and the value will be how many of that item is
being added. If the key is not already contained in the tree it will be inserted as a new node. If the pair is already 
contained in the tree, the value of the attempted insertion will be added to the value of the existing node.

```
multiSetInsert(key, value) {
    Check if the key is already in the tree with AVLTree contains method {
        If it is, set the key pair's value to currentValue + value
    }
    Else (If the key is not in the tree {
        use AVLTreeInsert to add the key pair to the tree
    }
}
```

### Erase



``

``

### Size



``

``

### Find



``

``

### Contains



## Set Operations

## Extension Feature

## UML Diagram

## Trade-off Analysis

## Alternative Design

## Evaluation Plan

## Conclusion

### References
Blizard, Wayne D. “Multiset Theory.” Notre Dame Journal of Formal Logic, vol. 30, no. 1, 1989, pp. 36–66,
https://projecteuclid.org/journalArticle/Download?urlid=10.1305/ndjfl/1093634995. Accessed 2 Dec. 2025.

“C and C++ Reference.” Cppreference.Com, cppreference,
https://cppreference.com/index.html. Accessed 2 Dec. 2025.