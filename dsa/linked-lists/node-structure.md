# Node Structure

```cpp
class Node{
    public:
        int data;
        Node* next;
    
    public:
        Node(int data1){
            data=data1;
            next=NULL;
        }
        Node(int data1,Node* next1){
            data=data1;
            next=next1;
        }
}
```