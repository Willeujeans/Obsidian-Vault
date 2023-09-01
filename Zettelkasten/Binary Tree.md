*System of nodes where each node has data and two children nodes, left and right.*
![[Pasted image 20230821171012.png]]

// Method 1: Using "struct" to make
// user-define data type
struct node {
    int data;
    struct node* left;
    struct node* right;
};
 
// Method 2: Using "class" to make
// user-define data type
class Node {
public:
    int data;
    Node* left;
    Node* right;
};