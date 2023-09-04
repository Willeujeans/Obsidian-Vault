Data stored in the "head" is compared with every array element one after another
![[LinearSearch.gif]]

```
int linearSearch(myArray, element){
 int head = element;
 for(int x = 0; x < myArray.length; x++){
  if(myArray[x] == head){
   return myArray[x];
  }
 }
}
```
