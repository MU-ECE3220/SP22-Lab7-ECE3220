# Week 8 | Lab 7 - Templates

Your assignment for this week is to implement a stack data structure using a template class. Provided for you below is a template *pun intended* for what your class should like.

# Primer
```c++
template<typename T> // could also be template<class whatever>
class StackList{
        public :
                struct StackNode{ // we define the StackNode class here so that it may use our template T.
                           // public space of StackNode   
                           Node(const T& nodeItem){//ToDo}
                           Node* next;
                           // "getter" for node item | 
                           //const following the parantheses indicates "const-correctness". 
                           // This guarantees that objects will not be mutated(modified) by this function "nodeItem()".
                           T nodeItem () const{/*ToDo*/ } /* - here is the aforementioned getter */

                    private:
                            T nodeItem_; // data item associated with a single node instance
                
                }; // end class StackNode
                 // continuing with class "StackList"
                List(){
                    head_->nodeItem_ = T{}; // initialize to default template value || whatever data type it assumes
                    /*ToDo More in here*/
                }

                List(const T& nodeItem){ // ToDo }
                bool isEmpty(){ // ToDO - returns true if stack is empty}
                void push_back(const T& nodeItem) { // ToDO - assigns element at the top of the stack}
                void pop(){ // ToDo deletes element at the top of the stack}
                void print_stack(){ /*ToDo*/ }
                void clear(){/*ToDo -- pops all items off the stack}
                int size() {/*ToDo -- returns the size of the stack*/}
};


```

# Assignment
Your lab assignment this week entails using a template class to design a stack data structure. Remember that a stack is a linear data structure which follows a LIFO(Last In First Out) or FILO(First In Last Out) ordering. Your should follow the linked list style of implementing your stack. A skeleton class has been provided for you to fill out. Keep in mind that you may need to have additional items/methods in the class or even different return types for the class functions/methods. You are the programmer so you may take some liberties. 
For your assignment, i'd like you to create four(4) different stacks :
        - An `int` stack
        - A `char` stack
        - A `float` stack
        - A `string` stack
- Each one of your stacks should contain five elements. You *may* place the first item in each stack using the `converting constructor` i.e. `StackNode( const T& nodeItem)` however, subsequent stack elements should be added using the `push_back()` method. 
- You should demonstrate that your `pop` method works correctly by performing two susbequent `pop` operations on the stack. Print the items in the stack along with the stack size.
- At the end of your program, you should demonstrate that your `clear` method works correctly by clearing each stack and printing the size and contents.
- Be sure to perform exception handling with try-catch clauses !!



# <span style="color:red">Warning</span>
<span style="color:red">Failure to heed the following statements may result in lost points.</span>
- Valgrind will be used on your assignments and be a critera for grading.
- Do not push unneeded files, such as those created during compilation.
- **NO SMART POINTERS ALLOWED** ... yet. 
- Test all of your functions in `main`.
- Use some exceptions for handling errors.
- After performing your final commit, get a fresh clone in a different folder to ensure your repository will compile and run for submission.
- If you only implement one additional set (a set of functions is defined as greater than or equal to four), half of the points will be deducted.

Example valgrind output that would not result in a loss of points:
```
==18852== 
==18852== HEAP SUMMARY:
==18852==     in use at exit: 0 bytes in 0 blocks
==18852==   total heap usage: 24 allocs, 24 frees, 3,952 bytes allocated
==18852== 
==18852== All heap blocks were freed -- no leaks are possible
==18852== 
==18852== For counts of detected and suppressed errors, rerun with: -v
==18852== ERROR SUMMARY: 0 errors from 0 contexts (suppressed: 0 from 0)
```
