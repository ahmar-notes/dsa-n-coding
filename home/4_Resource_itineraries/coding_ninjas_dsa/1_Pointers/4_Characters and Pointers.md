# 4. Characters and Pointers

A character array behaves different than other arrays.

Difference 1:

The printing of array is different as:

Int a[] = {1,2,3}

Int char[] = "abc";

Cout << a << endl;

Cout << char << endl;

Output: 780 (suppose address of a[0] or a)

 abc

Here, literally the whole character array is printed out.

(character array's elements can be declared in the above way as well)

Difference 2:

When a character pointer is initialized with address of a character array, if we try to print the pointer, generally it would have printed the address, but here:

Char c1 = 's';

Char *pc = &c1;

Cout << c1 << endl;

Cout << pc << endl;

Output: s

 s*?@$ (garbage after s)

When the pointer pc is called it goes to the c1's character (here 's'), and prints until '\0' is not encountered, hence the garbage.

Difference 3:

If a character array is initialized with characters, First the input/elements of the array is stored in temporary memory before giving a special memory block as an array. But when a character pointer is initialized with characters. Then again temporary memory is storing the data/elements, but now the pointer starts pointing to the memory location of the temporary memory, which can be dangerous.