# 3. Dynamic Memory Allocation

### Why?
- Whenever we make an array, we are obliged to define the number of element it is going to store. And if we make an array with variable size, it raise error.
* Another benefit is that, if an array is made, but only a fraction of part is used, the remaining memory is getting wasted, but in a dynamic memory size can be reduced accordingly.
* Even if a variable is out of scope, the variable is not deleted. And can be problem, because the memory is needs to be deleted manually.

There are 2 types of memory available with the program to use while running a program:
- Stack (relatively smaller in size)
- Heap (relatively bigger in size)

### Stack
It is the type of memory majorly used when running a program. Generally all variables that are declared are stored in Stack. Stack adjust its size while compiling based on the number and type of variable that are declared. And it has exact same size of memory as required, so whenever we need an array of variable size, stack can't decide how much memory to allocate and hence raise error.
Here automatic deletion of memory is performed once the memory has gone out of scope.
This is called **Static memory allocation**.

### Heap
It is another type of memory, but being relatively larger in size, and dynamic in size, it can handle any size of variable, and allocate memory respectively. Unlike Stack, Heap allocated memory on run time, and hence can allocate variable sized arrays. And if a variable needs to be declared for using heap memory, a new keyword is used i.e. "new".

But unlike stack, in Heap a variable is doesn't consist of a name, whereas when the variable is declared, it return the variable's memory's address. So we need to store the address of the heap variable in a pointer, without storing the address, the variable is useless.

***Syntax:***
```c++
data_type *variable_name = new data_type;
```
Obviously, both datatypes must be same.

As the memory is never deallocated automatically, and hence the memory needs to be deleted manually, the deleting syntax is:

***Syntax:***
```c++
delete variable_name;
```

But there is a little special syntax to delete an array:
```c++
delete [] variable_name;
```

**Note:** In above syntax, the pointer in **not** deleted, instead only the variable in heap is being deleted. And if not deleted, and the memory limit is reached, the program/app might crash.


