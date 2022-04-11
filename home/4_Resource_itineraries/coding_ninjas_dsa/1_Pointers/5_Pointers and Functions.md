# 5. Pointers and Functions

Generally, functions are passed by values/call by value. So if we change our pointer in another custom function, the action performed will not affect our actual pointer.

**Example:**

```c++
void increment(int *p)
 {
	 p = p + 1;
 }
 
 int main()
 {

	 int i = 10;
	 int *pi = &i;
	 cout << p << endl;
	 increment(p);
	 cout << p << endl;
	 return 0;
 }
```

Output: (e.g. Address of i -> 679)
			    679
	            679

If a custom function changes the value of i by going to the address (p & pi), the value of i can be changed in overall environment.

**Note:** When an array is passed in a custom function, the array passes as pointer not as an array.

**Example:** 

```c++
void sum(int a[], int size)
{
	cout << sizeof(a) << endl;
}

int main()
{
	int a[10];
	cout << sizeof(a) << endl;
	cout << sum(a, 10);
	return 0;
}
```

Output: 40
              4 (4 or 8 bytes for pointer)

*Idea:* Use a for loop for getting all the characters in the custom function, by incrementing the pointer of first element (here a[] or * a).