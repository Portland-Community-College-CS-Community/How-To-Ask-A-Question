# How To Ask A Question


There is no such thing as a dumb question. We are all learning and no one is born a computer scientist. With that being said, it is good practice to learn **how** to ask effective questions in a programming context. Asking a well-formed question **will** yield a working solution from the community.


Here is a general framework for asking questions:


1.  Clearly define what your problem is. (What are the inputs? What is the desired output?)

2. Google your problem. Research the problem a little before asking.

3.  Make a minimal reproducible example. This means abstracting the problem in a way where someone else can easily understand what you are trying to do without needing to understand the context of your entire program.

4. Ask your question! 


Consider the example of a segfault using the framework from above

1)  My program is hitting a segfault at runtime. I have confirmed that the segfault happens at line 12 inside of my forloop.
2) Google "What is a segfault?", "My program is segfaulting", "How do I stop a segfault?"
3) Create a **minimal reproducible example**:
```c++

class MyClass {
/*
.  // a bunch of implementation details
.
.
*/
};

using namespace std;
int main() {
	MyClass c(1,2,3,4);
	// more implementation details
	// ..
	// ..
	for(int i = 0; i < c.size(); i++) {
		cout << c.at(i) << endl;      // segfaults for some value i for c.at(i)
	}
}
```
There is a **TON** of extra implementation detail that may or may not be related to your actual issue. 

Consider "distilling" the problem to a **minimal reproduciple example** such as

```c++
class Foo {
    int at(int i) { /* implementation of at() */ }
    int size() { /* implementation of size() */ }
};

int main() {
	Foo foo(1,2,3,4);
     for(int i = 0; i < foo.size(); i++) {
	     cout << foo.at(i) << endl;
     }
}
```

The above example shows taking out the parts of the problem that is not nessecary for diagnosing and fixing the bug.

4) Ask my question!


Helpful links: 

How to use a debugger: (link)[https://stackoverflow.com/questions/25385173/what-is-a-debugger-and-how-can-it-help-me-diagnose-problems]

How to ask a good question: (link)[https://stackoverflow.com/help/how-to-ask]
