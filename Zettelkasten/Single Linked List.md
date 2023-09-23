
![[Pasted image 20230922112512.png]]
## Node Class
```
class Node {
public:
   int data;
   Node* next;

   Node(int initialData) {
      data = initialData;
      next = nullptr;
   }
};
```
## LinkedList Class
```
class LinkedList {
private:
   Node* head;
   Node* tail;
   
public:
   LinkedList() {
      head = nullptr;
      tail = nullptr;
   }
};
```
## Appending
```
void Append(Node* newNode) {
   if (head == nullptr) {
      head = newNode;
      tail = newNode;
   }
   else {
      tail->next = newNode;
      tail = newNode;
   }
}

int main(){
	Node* nodeA = new Node(42);
	numList.Append(nodeA);
	return 0;
}
```
## Prepending
```
void Prepend(Node* newNode) {
   if (head == nullptr) {
      head = newNode;
      tail = newNode;
   }
   else {
      newNode->next = head;
      head = newNode;
   }
}
```
## Remove
```
ListRemoveAfter(list, curNode) {
   // Special case, remove head
   if (curNode is null && list->head is not null) {
      sucNode = list->head->next
      list⇢head = sucNode

      if (sucNode is null) { // Removed last item
         list->tail = null
      }
   }
   else if (curNode->next is not null) {
      sucNode = curNode->next->next
      curNode->next = sucNode

      if (sucNode is null) { // Removed tail
         list->tail = curNode
      }
   }
}
```
## Search

