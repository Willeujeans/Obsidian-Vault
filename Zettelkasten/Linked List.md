*System of nodes that make use of the [[Pointer]], nodes store data and a pointer to another node*

## Single Linked List
*navigation is forward only*
Made from a collection of nodes
nodeStructure = {data:"gamer", link: nodes[3]}

## Doubly Linked List
*navigation is forward & backward*

## Circular Linked List
*last element is linked to the first*

```
struct Node{
	string data;
	struct Node *next;
}

int main(){
	struct Node *one = NULL;
	struct Node *two = NULL;
	struct Node *three = NULL;
	
	one = new Node;
	two = new Node;
	three = new Node;
	
	one->data = 15;
	two->data = 22;
	three->data = 19;
	
	one->next = two;
	two->next = three;
	three->next = NULL;
}
```
