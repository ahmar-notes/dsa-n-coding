# 1. Introduction to Pointers

Pointers are special type of variable which stores the address of other variables. To get initialize the address of the variable we use "&" operator or "address of" operator. The pointer is also written with the same datatype whose address it is pointing to. Address of variables are Hexa-Decimal. The size of pointer variable is 4 or 8 bytes according to the system, but irrespective of the variable's data type which its pointing towards.

Syntax:

data_type *variable_name = &variable;

Here &variable is giving address of the variable.

Example:

int i=0;

int *point = &i;

Or

Int * point = &i;

Or

Int* point = &i;

cout << point << endl;

" * " is only used for creating the variables, and further can be used just like any normal variable.

Accessing variables from address:

The value of a variable can be accessed via its address by using pointers. We store/print the value in pointer, then by using "*" operator we can access the value stored at that address.

Example:

Int i = 0;

Int *pi = &i;

cout << *pi << endl;

Output : 0

So, *variable will automatically store/print address of the variable it is pointing to once the pointer is declared.

i.e *p = i = 0.

Note:

The "int *pi" is for declaring the pointer and "cout << *pi << endl" here for accessing the value of the variable.

Note: 

Never leave create a pointer with garbage address (non-initialized), and if some operations is applied to that memory location, that can be harmful and unwanted. Must initialize a pointer with the desired address or at least point toward null (int *p = NULL or int *p = 0) i.e. it point to nothing or null.

Note:

 We cannot assign value directly to null pointer's value.

Example:

Int *ptr = 0;

Int a =10;

*ptr=a;

Output: Error
