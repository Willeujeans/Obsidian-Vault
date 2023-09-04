Breaks array in half until the element is found, array must be sorted
![[BinarySearch.gif]]

```
BinarySearch(numbers, numbersSize, key) {
   mid = 0;
   low = 0;
   high = numbersSize - 1;
   
   while (high >= low) {
      mid = (high + low) / 2;
      if (numbers[mid] < key) {
         low = mid + 1;
      }
      else if (numbers[mid] > key) {
         high = mid - 1;
      }
      else {
         return mid;
      }
   }
   return -1 // not found
}
```