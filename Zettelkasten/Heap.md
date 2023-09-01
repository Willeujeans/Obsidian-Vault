Max Heap: A tree based data structure where the children  <= parent.

Min Heap: A tree based data structure where children >= parent.

A heap in an array format

          $[21]$
       __ | __
     |             |
   $[17]$        $[15]$
  _ | _       _ | _
 |       |      |       |
 $[8]$  $[5]$   $[1]$

$[0,21,17,15,8,5,1]$

leftChild$i$ = $2*i$
rightChild$i$ = $2*i +1$
parent$i$ = $floor(i/2)$

Creating a Max-heap from an unordered array
O(logn)
```
maxHeapify(a, heapSize, i){
	var left=2*i;
	var right=2*i+1;
	
	var largest = i;
	
	if(left<heapSize && a[i]){
		largest = left;
	}
	
	if(right<heapSize && a[right] > a[largest]){
		largest = right;
	}
	
	if(largest != i){
		var storage = a[i];
		a[i] = a[largest];
		a[largest] = storage;
		maxHeapify(a,heapSize,largest)
	}
	
}
```

