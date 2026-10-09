# Linked List Cycle

## Problem
Determine if a linked list has a cycle. Return `true` if it does, `false` otherwise.

## Approach
Floyd's Algorithm (Two Pointers):
1. `slow` moves 1 step, `fast` moves 2 steps.
2. If `fast` or `fast.next` is `null` -> no cycle (`false`).
3. If `slow == fast` -> cycle detected (`true`).

### Tracing
`[3, 2, 0, -4]`, loop `-4 -> 2`

* **Start:** `slow` = 3, `fast` = 3
* **Step 1:** `slow` = 2, `fast` = 0
* **Step 2:** `slow` = 0, `fast` = 2
* **Step 3:** `slow` = -4, `fast` = -4 (`slow == fast` -> `true`)

## Complexity
* **Time:** $O(n)$ — `fast` traverses at most $n$ nodes.
* **Space:** $O(1)$ — only 2 pointers used.

## Reflection
* **Optimality:** $O(n)$ time and $O(1)$ space is already optimal.
* **Alternative:** `HashSet` checks visited nodes in $O(n)$ time, but uses $O(n)$ space.
