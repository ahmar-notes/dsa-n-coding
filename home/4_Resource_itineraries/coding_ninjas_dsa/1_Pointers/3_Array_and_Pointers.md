# 3. Array and Pointers   

Array is collection of elements. It has contiguous memory. It has similar properties as pointers and has data type as same as the elements stored in it.

Syntax:

data_type variable_name[number of elements];

Number of elements isn't mandatory to specify.

Example:

Int a[10];

a[0] = 5;

Cout << a[0] << endl;

Cout << *a << endl;

Output: 5

 5

Note:

As above, 'a' is similar to a pointer that points to first element of the array. Hence, a[0] and *a prints same value.

Pointer arithmetic can be applied on a for desired output.

The accessing of values can also be performed on the further elements of the array.

Example:

Int a[10];

a[1]=4;

cout << a[1] << endl;

cout << *(a+1) << endl;

Output: 4

 4

Note: *(a + 1) is same as a[1].

Or

*(a + i) = a[i]

And a[i] is syntactic sugar for *(a+i)

Note: Even i[a] = a[i] because both are referring/pointing to the same address.

i.e. i[a] = *(i + a) and a[i] = *(a + i), and both memory location (a + i) and (i + a) are same.

Even thought it seems that pointer and array are same, they have some differences.

Difference 1: The " sizeof( ) " function the size of that object. But as seen above, 'a' is basically address of a[0]. It seems like a is a pointer but when sizeof function is performed the size of a[] is the actual size of all elements combined that are stored in the array, whereas if it would be just a pointer the size would have been 8 or 4 bytes as pointers.

Int arr[10]

40 bytes

Int *I

4 or 8 bytes

Difference 2: The '&' operator works different for pointers and array. When a pointer is declared a separate memory is allocated to store the address of the pointed variable, whereas in array the address of the first elements is stored in the symbol table not in separate memory. And when we print or see the address of the pointer itself it shows its own separate memory's location.

In,

Int a[10];

Cout << a << endl;

Cout << &a << endl;

Output is the same, i.e. address of the first element or the starting of the array.

Whereas,

Int *p = &a;

Cout << p << endl;

Cout << &p << endl;

Output: The first line would be the address of the 'a'.

 Then second line would be the address of the separate memory allocated to the pointer.

Difference 3: The address stored in a pointer can be reassigned/changed as a normal value, whereas in array 'a' which seems like a pointer pointing to a[0] cannot be reassigned/changed. The reason is that the address that is stored in pointer is stored in a separate memory, but not in case of arrays.

Int *p=&a[0];

p = &a[4];

Here, first we assigned the address of a[0] to the pointer then replaced it with the address of a[4], but

a = a + 4;

Raise an error.