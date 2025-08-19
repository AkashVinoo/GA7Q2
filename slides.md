---
marp: true
theme: product-docs
class: lead
paginate: true
footer: "Page ${page} / ${total}"
math: katex
---

# Product Documentation Presentation
### Technical Writer:  
📧 **24f2000935@ds.study.iitm.ac.in**

---

## Introduction

- This presentation demonstrates product documentation using **Marp**.  
- Features included:
  - Custom theme  
  - Page numbers  
  - Background image  
  - Custom styling  
  - Mathematical equations  
  - Version-control ready  

---

## Background Image Example
<!-- _backgroundImage: url('https://picsum.photos/1280/720') -->
<!-- _backgroundSize: cover -->
<!-- _color: white -->

### Slide with Background Image  
This slide uses a full background image with custom styling.  
📧 Contact: **24f2000935@ds.study.iitm.ac.in**

---

## Algorithmic Complexity

We often analyze runtime using *Big-O* notation:

$$
T(n) = O(n \log n)
$$

Example: Merge Sort has time complexity $O(n \log n)$.

---

## Code Sample

```python
def binary_search(arr, target):
    left, right = 0, len(arr) - 1
    while left <= right:
        mid = (left + right) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1
