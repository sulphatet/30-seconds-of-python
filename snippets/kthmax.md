---
title: kth max value
tags: list,recursion
expertise: intermediate
firstSeen: 2022-04-29T00:26:12+05:30
---

Returns the value of the k-th greatest element in a given list.

- Recursively deletes the largest element in the list and decrements the value of `k`.
- The base case is hit when `k` is `1` and the problem reduces to finding the greatest element in the list.

```py
def kthmax(k, list):
    if (k == 1):
        return max(list)
    else:
        m = max(list)
        return(kthmax(k-1, [x for x in list if x != m]))
```

```py
kthmax(3,[4, 6, 2, 7, 3, 2, 6, 6]) # 4
```
