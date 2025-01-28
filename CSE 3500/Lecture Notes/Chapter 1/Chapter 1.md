
# Insertion Sort (A,n)

```
for i =2 to n
	key = A[1]
	// Insert A[i]into the sorted A[1:i-1]
	j i-1 
	while j<0 and A[j]>key
		A[j+1]= A[j]
		j=j-1
	A[j+1]=key
![[Recording 20250123094606.m4a]]

```
![[20250123_094034.jpg]]
![[20250123_094034.jpg]]
![[20250123_094034.jpg
![[20250123_094821.jpg]]
![[Recording 20250123094935.m4a]]
![[20250123_095544.jpg]]
Worst Case
![[20250123_100718.jpg]]![[20250123_100720.jpg]]

Average Case:
*i*/2

We will mainly be focusing on worst case it the celling of the running time would be.
$$
\frac{a}{b}
$$


Rate of growth
$$
\frac{n^2}{100} +100n^1+17n*n^0
$$






# Merge Sort Divide and Conquer
![[20250123_102001.jpg]]
![[20250123_102223.jpg]]
Merge will be O(n).
![[20250123_103733.jpg]]

![[20250123_104134.jpg]]

![[20250123_104138.jpg]]
![[Recording 20250123104340.m4a]]
## 1/28
![[Pasted image 20250128094100.png]]
 Recurrence for merge sort  We shall usually omit to state the base case when T(n)= theta (1) sufficiently small n, but only when it does not affect the asymptomatic solutions to the recurrence. 
 ![[20250128_094417.jpg]]
  nlog(n) vs n^2
  Log(n) how many times do you need to divide n by 2 in order to get to 1?
  nlog(n) grow more slowly than n^2 , there fore merge sort asymmetrically beasts insertion sort in the worst case.  
Worst case  analysis provides a guarantee or upper bound on per performance bound holds for every input. we mande no assumptions about the  distributing of input.
Ignore constant factors and low-order terms
- way easier
- uses very little predictive power
- often machine and language dependent
Asymptotic analysis
- Focus on running time for large inputs sizes
- selection of the algorithm 

What is a fast algorithm
- worst case running time grows slowly with input size
- Holy grail: linear running or close to it.
	- can we have algorithms that run in less than linear times

# Chapter 3
Concentrated on running tum and the order of growth rate.
	runt times primarily depends on the highest order terms. Therefore for asymptotic analysis we ignore lower order terms. can be use to characterize mem requirements.

For a function \( f(n) \), asymptotic notation is formally defined as:

1. **Big-O Notation (Upper Bound)**:
   - \( f(n) \) grows **at most** as fast as \( g(n) \).
   - Formal definition:
     $$
     f(n) = O(g(n)) \quad \Leftrightarrow \quad \exists c, n_0 > 0 \text{ such that } f(n) \leq c \cdot g(n), \forall n \geq n_0.
     $$

2. **Omega Notation (Lower Bound)**:
   - \( f(n) \) grows **at least** as fast as \( g(n) \).
   - Formal definition:
     $$
     f(n) = \Omega(g(n)) \quad \Leftrightarrow \quad \exists c, n_0 > 0 \text{ such that } f(n) \geq c \cdot g(n), \forall n \geq n_0.
     $$

3. **Theta Notation (Tight Bound)**:
   - \( f(n) \) grows **exactly** at the rate of \( g(n) \).
   - Formal definition:
     $$
     f(n) = \Theta(g(n)) \quad \Leftrightarrow \quad \exists c_1, c_2, n_0 > 0 \text{ such that } c_1 \cdot g(n) \leq f(n) \leq c_2 \cdot g(n), \forall n \geq n_0.
     $$
![[20250128_095736.jpg]]
![[20250128_100550.jpg]]
![[20250128_100638.jpg]]
![[20250128_100756.jpg]]
