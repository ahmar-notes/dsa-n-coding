# 2. Pointer Arithmetic

Just like any other variable, any arithmetic operation can be performed on pointer variables too.

The operations on pointers lead to other memory location based on the performed operation.

Example:

Int a = 10;

Int *pa = &a;

pa+=1;

cout << pa << endl;

Output:

245

249

Assume the address of a is 245. Adding one to the address in the pointer will make a jump of 1 int storage capacity (i.e. 4 or 8 bytes). And will point on new address.

Similarly other operations will be performed.

Note:

The memory allocated for variable may not be contiguous or consecutive to each other and the new address may lead to unknown variables.

Conclusion:

 The only application of pointer arithmetic can be if the memory allocated to the program variables are contiguous, as in array.