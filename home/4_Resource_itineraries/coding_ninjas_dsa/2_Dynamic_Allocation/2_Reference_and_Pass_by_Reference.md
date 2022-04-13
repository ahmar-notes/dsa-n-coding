# 2. Reference and Pass by Reference

Reference is a type of variable who does not have its own memory allocated. It refers or have the same address of a variable in the symbol table, i.e. like having two names for a single person.
<ins>This result in using memory efficiently.</ins>
A reference variable must be assign with the desired variable at initializing (else error).

**Example:**

```c++
int i=10;
int &j = i;
i++;
cout << i << endl;
cout << j << endl;
```

Output: 
			 11
			 11

i.e.
	Symbol table              memory allocated
	i -> 950                       location : 950
	j -> 950                       i -> |10|

*<ins>Note:</ins>* Changes in original value of the variable (here ' i ' ) can be see in the value of reference variable (here ' j '), as they have same memory.

**Use:** A reference variable can be used to pass the variables from main into a function, that can perform action on the main's variable. Here is how:

```c++
void increment(int &n)
{
	n++;
}

int main()
{
	int i=10;
	cout << i << endl;
	increment(i);
	cout << i << endl;
}
```

Output: 10
              11

Originally, if we pass normal variable (here int), the n++ would have been applied to a local variable of that function that doesn't affect the original variable i.
We can also use a function with return action, but that leads to extra memory usage.

If we make a function whose return type in by reference, then we must be careful, that once the function is out of focus, the scope of the variables in the function will be over, hence no effect on the variable's value in main's scope.

```c++
int &increment(int n)
{
	 n++;
	 return n;
}

int main()
{
 int i=10;
 int &k=increment(i);
 cout << i << endl;
}
```

Here, the compiler raise an error as "reference to local variable returned", i.e. It will not affect 'i'.

***Note: (bad practice)***-> Never try returning a pointer or a reference variable from a function, cause they get out of scope as soon as the function is over, and the respective memory is removed/deleted/not in scope.