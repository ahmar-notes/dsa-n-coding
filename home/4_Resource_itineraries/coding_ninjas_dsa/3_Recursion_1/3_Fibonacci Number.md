# 3. Fibonacci Number

Recursive Algorithm to find the nth Fibonacci Number: (The series starting from 0,1,1,2 and 0 as the 0th element)
```c++
int fib(int n)
{
	// Base case: 1
    if(n==0)
        return 0;

	// Base case: 2
    if(n==1)
        return 1;
    
    int num1 = fib(n-1);
    int num2 = fib(n-2);
    return num1+num2;
}

int main()
{
    int n;
    cin >> n;
    int i = fib(n);
    cout << i << endl;
}
```

Here, we needed two base case because, 
**Example:**
		If `fib(n-2)`, when n is odd, might not lead to the base case of `n=0`. Hence, to avoid that we added "base case: 2" to have a base case for odd n values.