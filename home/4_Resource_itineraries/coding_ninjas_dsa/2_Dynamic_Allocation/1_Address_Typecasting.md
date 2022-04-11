# 1. Address Type-Casting

**Q.** Why we need to write int* or char* etc for declaring pointer, why can we have a new 
	datatype for pointers?

**Ans**-> We need int* or char* because:
- if we have the initial address of a variable, we must know how many bytes further we need to read/write and the data type of the variable defines the size of variable. 

- The second reason is that every data is interpreted according their format such as float, int etc, so providing the data-type to pointer result in the interpretation of the value stored in the variable.

If we initialize a literal/number to a char variable, it automatically converts the number into respective ASCII character. This automatic conversion is called automatic/implicit type casting.

In case of pointers, if char pointer is initialized with an int pointers, the automation fails/error. Unlike implicit type casting, here we need to explicitly mention in what type we want to cast the int pointer for initializing it in char pointer, hence called as explicit typecasting.

**Example:**

```c++
// Implicit Type-casting
int i = 65;
char c = i; 

// Explicit Type-casting
int *p = &i;
char *pc = (char*)p;

// Char pointer byte allocation system
cout << *pc << endl;
cout << *(pc+1) << endl;
cout << *(pc+2) << endl;
cout << *(pc+3) << endl;
```

Output: A
			  (blank/NULL)
			  (blank/NULL)
			  (blank/NULL)

(Not sure) But, the value 65 is not stored in the memory as: 
	i -> |0|0|0|65|
	This above system in Big Endian system i.e. the biggest number/data is present in last of the memory allotted.

(Not sure) Whereas actually the number is stored as:
	**i -> |65|0|0|0|**
	This system is called as Little Endian system i.e. the largest number/data is stored first. 

In case of char pointers little Endian system is applied.

