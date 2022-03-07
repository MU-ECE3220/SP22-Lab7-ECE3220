# Week 8 | Lab 7 - Templates

This week assignment is to implement a templated stack class.

# Primer
```c++
template<typename T> // could also be template<class whatever>
class StackList{
        public :
                struct StackNode{ // we define the StackNode class here so that it may use our template T.
                           // public space of StackNode   
                           Node(T nodeItem){//ToDo}
                           Node* next;
                           // "getter" for node item | 
                           //const following the parantheses indicates "const-correctness". 
                           // This guarantees that objects will not be mutated(modified) by this function "nodeItem()".
                           T nodeItem () const{/*ToDo*/} - here is the aforementioned getter 

                    private:
                            T nodeItem_; // data item associated with a single node instance
                
                }; // end class StackNode
                 // continuing with class "StackList"
                List(){
                    head_->nodeItem_ = T{}; // initialize to default template value || whatever data type it assumes
                    /*ToDo More in here*/
                }

                List(T nodeItem){ // ToDo }
                bool isEmpty(){ // ToDO - returns true if stack is empty}
                void push_back(T nodeItem) { // ToDO - assigns element at the top of the stack}
                void pop(){ // ToDo deletes element at the top of the stack}
                void print_stack(){ /*ToDo*/ }
                void clear(){/*ToDo -- pops all items off the stack}
};


```
