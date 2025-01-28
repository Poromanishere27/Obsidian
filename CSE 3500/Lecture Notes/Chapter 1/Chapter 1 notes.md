### **Insertion Sort**

#### **Overview:**

Insertion Sort builds the sorted array one item at a time. It works similarly to sorting playing cards in your hand:

- Start with one card.
- Take the next card and insert it in the correct position relative to the sorted cards.

#### **Pseudocode:**
```
for i = 2 to n
    key = A[i]
    // Insert A[i] into the sorted A[1:i-1]
    j = i - 1
    while j >= 0 and A[j] > key
        A[j + 1] = A[j]
        j = j - 1
    A[j + 1] = key

```
#### **Example (Step-by-Step for A = [5, 3, 4, 1]):**

1. Start with the second element (`3`):
    
    - Compare with `5`, insert `3` before `5`.
    - Array becomes: `[3, 5, 4, 1]`.
2. Next, consider `4`:
    
    - Compare with `5`, move `5` one position right.
    - Compare with `3`, insert `4` after `3`.
    - Array becomes: `[3, 4, 5, 1]`.
3. Lastly, consider `1`:
    
    - Compare with `5`, `4`, and `3`, move all three to the right.
    - Insert `1` at the beginning.
    - Array becomes: `[1, 3, 4, 5]`.

#### **Complexity:**

- **Best Case (Array already sorted):** O(n)O(n)O(n).
- **Worst Case (Array sorted in reverse):** O(n2)O(n^2)O(n2).
- **Average Case:** O(n2)O(n^2)O(n2) due to the nested loop.

---

### **Merge Sort**

#### **Overview:**

Merge Sort is a divide-and-conquer algorithm:

1. **Divide:** Split the array into two halves.
2. **Conquer:** Recursively sort each half.
3. **Combine:** Merge the two sorted halves.

#### **Pseudocode:**
```
function mergeSort(A, left, right)
    if left < right
        mid = (left + right) / 2
        mergeSort(A, left, mid)
        mergeSort(A, mid+1, right)
        merge(A, left, mid, right)

```
#### **Merge Step (Combining Two Sorted Arrays):**

- Merge two sorted arrays into a single sorted array by comparing elements one by one.

#### **Example (Step-by-Step for A = [5, 3, 4, 1]):**

1. Divide the array:
    
    - Split `[5, 3, 4, 1]` into `[5, 3]` and `[4, 1]`.
    - Further divide `[5, 3]` into `[5]` and `[3]`, and `[4, 1]` into `[4]` and `[1]`.
2. Conquer (Sort subarrays):
    
    - `[5]` and `[3]` are already sorted; merge them into `[3, 5]`.
    - `[4]` and `[1]` are already sorted; merge them into `[1, 4]`.
3. Combine:
    
    - Merge `[3, 5]` and `[1, 4]` into `[1, 3, 4, 5]`.

#### **Complexity:**

- **Time Complexity:** O(nlog⁡n)O(n \log n)O(nlogn) for all cases (best, average, worst).
- **Space Complexity:** Requires additional memory for merging.

---

### **Visual Diagram**

#### **Insertion Sort Diagram (Example for A = [5, 3, 4, 1]):**
```
Initial: [5, 3, 4, 1]
Step 1: [3, 5, 4, 1]  (Insert 3)
Step 2: [3, 4, 5, 1]  (Insert 4)
Step 3: [1, 3, 4, 5]  (Insert 1)

```
Merge Sort Diagram (Example for A = [5, 3, 4, 1]):
```
Divide: [5, 3, 4, 1]
        /          \
     [5, 3]      [4, 1]
     /   \        /   \
   [5]   [3]    [4]   [1]

Conquer: [3, 5]   [1, 4]

Combine: [1, 3, 4, 5]

```
