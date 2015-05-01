# runyourcode

## What
Just like gist, but it can run to get expected result, and you can package necessary env to run locally.  
Some idea like http://ideone.com/  
But, it will include:  
1. dependent lib  
2. compiler and related options  

I hope there can be checkbox there to help simplify these things.  
Also, when you are not sure which to choose, just type in searchbox to get matches.  


## Why
Why not online judge?  
As I know, what I need most daily is something like gist, not onlinejudge.  
However, gist can't run and besides code, there are many aspects, like os/compile/makefile.  
Deep in heart, I treat coding a mixture of kinds of trival things aside from code itself.  

Why not http://ideone.com/?  
However, you need to handle header file by yourself.  
Also, if additional lib is required, it also fails.  
That will be my first todos.  


## How
Leave todo here...  
Some references:
### http://ideone.com/
### http://www.codechef.com/ide
### http://www.zhihu.com/question/20343652?rf=20772489  
prefer to use docker when run code in sandbox  



Below cases fail in http://ideone.com/  
I hope to run them with runyourcode.  

### Case 1, requires necessary header file  
using namespace std;  
int main() {  
  vector<int> v;  
  v.push_back(10);  
  cout << v.size() << endl;  
  return 0;  
}  

### Case 2, requires compile options -pthread
void print_message_function ( void *ptr ) {  
  pthread_exit(0);  
}  
   
int main() {  
  // your code goes here  
  void *data1;  
  void *data2  
  pthread_t thread1, thread2;  
  pthread_create (&thread1, NULL, (void *) &print_message_function, (void *) data1);  
  pthread_create (&thread2, NULL, (void *) &print_message_function, (void *) data2);  
  
  pthread_join(thread1, NULL);  
  pthread_join(thread2, NULL);  
  return 0;  
}  

