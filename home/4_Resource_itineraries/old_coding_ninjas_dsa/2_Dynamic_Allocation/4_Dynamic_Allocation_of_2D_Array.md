# 2. Dynamic Allocation of 2D Array

### Why?
We **cannot** declare 2d array as = new int[10]  [20 ] in Heap. So to create a 2D array, here is how:

### How?
1. We will make many 1D arrays using a loop. These arrays will be of the number as desired number of rows. And each array has capacity same as desired number of column; 
2. But by the above process we will be needing many pointer variables, so instead we make a pointer Array for storing the heap's variable's address, i.e. to store the address of heap variables, we need to make an array of pointers of variable size, we again need that array to be made in heap memory.
3. Hence the pointer array must be stored in a double pointer.

***Syntax:*** (General) 
 ```c++
 int m,n;
 cin >> m >> n;
 // declaring double pointer to store the array pointer.
 int **p = new int*[j];

 // Pointing the new variable of columns, running it rows number of time.
 for(int i = 0; i < m; i++)
 {
	 p[i] = new int[n];
	 // Getting input for the array element in the respective row and column.
	 for(int j = 0; j < n; j++)
	 {
		 cin >> p[i][j];
	 }
 }
 ```

Now once we have successfully made the 2D array in heap. We need to **manually delete** the memory allocated. Let's see how:
```c++
for(int i = 0; i < m; i++)
{
	//Deleting elements
	delete [] p[i];
}
delete [] p;
```

***Note: (blunder)*** -> Never delete p or the double pointer before p[i] or the 2D array, because once pointer is deleted first, we don't have the address of the array elements anymore, and it will be **impossible** to delete the memory.


