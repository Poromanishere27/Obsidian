
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
