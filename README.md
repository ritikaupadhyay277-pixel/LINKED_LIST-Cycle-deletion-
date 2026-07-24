# Detect a Cycle in a Linked List

## Problem Statement

Given the head of a singly linked list, determine whether the linked list contains a cycle.

A linked list is said to contain a cycle if a node can be reached again by continuously following the `next` pointer.

Return:

- `true` (1) if the linked list contains a cycle.
- `false` (0) otherwise.

---

## Approach

This solution detects cycles by storing the address of every visited node in an `unordered_set`.

### Algorithm

1. Create an `unordered_set` to store visited node addresses.
2. Traverse the linked list from the head.
3. For each node:
   - If the node's address already exists in the set, a cycle has been detected.
   - Otherwise, insert the node into the set and continue traversing.
4. If traversal reaches `NULL`, no cycle exists.

---

## Algorithm Used

- Hashing (`unordered_set`)
- Singly Linked List Traversal

---

## Complexity Analysis

| Operation | Complexity |
|-----------|------------|
| Time | **O(n)** |
| Space | **O(n)** |

Where **n** is the number of nodes in the linked list.

---

## Features

- Efficient linear-time traversal.
- Simple and easy-to-understand implementation.
- Uses node addresses instead of node values, ensuring accurate cycle detection.
- Handles empty lists and non-cyclic lists correctly.

---

## Sample Illustration

### Input

Linked List:

```
1 → 2 → 3 → 4
      ↑     ↓
      └─────┘
```

### Output

```
True
```

---

## HackerRank Challenge

**Problem:** Detect whether a Linked List contains a Cycle

https://www.hackerrank.com/challenges/detect-whether-a-linked-list-contains-a-cycle/problem

---

## Repository Structure

```
.
├── Solution.cpp
└── README.md
```

---

## Learning Outcomes

This problem helps in understanding:

- Singly Linked Lists
- Pointer manipulation
- Cycle Detection
- Hash-based data structures
- Time and Space Complexity Analysis

---

## Alternative Approach

A more space-efficient solution uses **Floyd's Cycle Detection Algorithm (Tortoise and Hare)**.

| Approach | Time | Space |
|----------|------|-------|
| Hash Set (Current Solution) | O(n) | O(n) |
| Floyd's Algorithm | O(n) | O(1) |

Although Floyd's algorithm is more memory efficient, the hash-set approach is intuitive and straightforward for understanding cycle detection.

---

## Language

- C++

---

## Author

**Ritika Upadhyay**

B.Tech CSE (AI & ML) | RGPV University
