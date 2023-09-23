The process of rearranging a list either into ascending or descending order.
## Code
### Outer loop
Runs the length of the array
### Inner loop
will compare and swap

## Bubble Sort - $O(N^2)$
A simple algorithm that will compare adjacent elements and move the smallest to the left
```
for i:0 to length(Array)
	for j:0 to length(Array)-i-1 
		if(array[j] > array[j+1])
			swap array[j] & array[j+1]

```

```
innerLoop
for j:0 to length(Array)-i-1 
//this is because the first i'th elements are sorted
```
## Selection Sort - $O(N^2)$
- We grab the lowest number and store it as our MIN
- we then cycle through the rest of the array looking for anything smaller
- If we find something smaller we store that as our MIN
- we then swap the first index after our sorted partition with the MIN
- we then move the sorted partition up 1

### Example
- array of {4,5,3,1}
- our MIN is 4
- we search
- our MIN = 3
- continue the search
- our MIN = 1
- we hit the end of the array
- MIN = 1 the end partition index is 0
- we swap MIN with partition index
- {1,5,3,4}
- repeat
- {1,3,5,4}
- {1,3,4,5}

```
void SelectionSort(int* numbers, int numbersSize) {
   for (int i = 0; i < numbersSize - 1; i++) {
      // Find index of smallest remaining element
      int indexSmallest = i;
      for (int j = i + 1; j < numbersSize; j++) {
         if (numbers[j] < numbers[indexSmallest]) {
            indexSmallest = j;
         }
      }
         
      // Swap numbers[i] and numbers[indexSmallest]
      int temp = numbers[i];
      numbers[i] = numbers[indexSmallest];
      numbers[indexSmallest] = temp;
   }
}
```

## Insertion Sort - $O(N^2)$
![[Pasted image 20230910160130.png]]
```
for i:1 to length(A)-1
	j=i
	while j>0 and A[j-1]>A[j]
		swapA[j] and a[j-1]
		j=j-1
```

