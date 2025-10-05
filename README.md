# Searching-algorithms

# 🔎 Searching Algorithms

## Theory

Searching algorithms are techniques used to find the location of an element (key or target) in a given dataset. They are broadly classified into two categories:

1. **Linear Search**
   - Traverses the array sequentially, element by element.
   - Compares each element with the target until it is found or the list ends.
   - **Time Complexity**:
     - Best Case: O(1) (element found at the first position)
     - Worst Case: O(n) (element at last position or not present)
   - **Space Complexity**: O(1)

2. **Binary Search**
   - Requires the input array to be **sorted**.
   - Repeatedly divides the search interval into two halves.
   - Compares the middle element with the target:
     - If equal → target found.
     - If smaller → search right half.
     - If larger → search left half.
   - **Time Complexity**:
     - Best Case: O(1)
     - Worst Case: O(log n)
   - **Space Complexity**: O(1) (iterative) or O(log n) (recursive)

**Summary:**
- Linear search works on both sorted and unsorted data but is slower.
- Binary search is faster but requires the data to be sorted.

---

## Algorithms

### 1. Binary Search (Iterative)
1. Start with a sorted array.
2. Initialize `low = 0` and `high = n-1`.
3. While `low <= high`:
   - Calculate `mid = (low + high)/2`.
   - If `array[mid] == target`, element is found.
   - If `array[mid] < target`, set `low = mid + 1`.
   - If `array[mid] > target`, set `high = mid - 1`.
4. If not found, return "Number not found".

---

### 2. Linear Search (Single Occurrence)
1. Start from the first element of the array.
2. Compare each element with the target.
3. If an element matches, print its index and stop.
4. If the end of array is reached without a match, print "Number not found".

---

### 3. Linear Search (Multiple Occurrences)
1. Start from the first element of the array.
2. Initialize an empty array/list to store indices of occurrences.
3. Traverse each element:
   - If `array[i] == target`, store index `i` in the list.
4. After traversal:
   - If list is empty → print "Not found".
   - Else → print all stored indices.

---

### 4. Linear Search Using Vector and Class
1. Define a class with a method for linear search.
2. Pass the array/vector and target to the method.
3. Traverse vector elements:
   - If match found → return index.
   - Else → return -1.
4. Print index if found; else print "Target not found".

---

## Conclusion

- Searching algorithms are essential for **locating elements** in datasets.  
- **Linear search** is simple, works on unsorted data, but can be slow (O(n)).  
- **Binary search** is much faster (O(log n)) but requires a **sorted array**.  
- Linear search can also be used to **find multiple occurrences** of a target.  
- Choosing the right search method depends on the **data size**, **order**, and **performance requirements**.


# 🔍 Comparison of Searching Algorithms

| Feature / Algorithm          | Linear Search (Single Occurrence) | Linear Search (Multiple Occurrences) | Binary Search (Iterative) | Linear Search using Vector & Class |
|-------------------------------|---------------------------------|-------------------------------------|---------------------------|-----------------------------------|
| **Data Requirement**          | Can be unsorted                | Can be unsorted                     | Must be sorted            | Can be unsorted                  |
| **Order of Search**           | Sequential                     | Sequential                          | Divide & Conquer          | Sequential                        |
| **Returns**                   | Index of first match           | Indices of all matches               | Index of match            | Index of first match              |
| **Time Complexity (Best Case)** | O(1)                           | O(1)                                 | O(1)                      | O(1)                              |
| **Time Complexity (Worst Case)** | O(n)                          | O(n)                                 | O(log n)                  | O(n)                              |
| **Space Complexity**          | O(1)                           | O(n) (for storing multiple indices)  | O(1)                       | O(1)                              |
| **Use Case**                  | Find a single element in small or unsorted data | Find all occurrences in unsorted data | Quickly find element in large sorted data | Encapsulation in class structure with dynamic arrays (vectors) |
| **Implementation Complexity** | Simple                         | Slightly more complex                | Moderate                  | Moderate                          |

---

## Summary

- **Linear Search (Single Occurrence)** → Simple, works on any array, stops at first match.  
- **Linear Search (Multiple Occurrences)** → Captures all indices, useful when element can appear multiple times.  
- **Binary Search** → Very fast on sorted data, uses divide-and-conquer.  
- **Linear Search using Vector & Class** → Demonstrates object-oriented approach with dynamic arrays, similar behavior to standard linear search.  

**Choosing an algorithm depends on:**
1. Whether the data is sorted or unsorted.  
2. Need for single or multiple occurrences.  
3. Dataset size and performance requirements.  
