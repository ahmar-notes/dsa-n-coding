# 1. Intro to Recursion
### Why
The advantages of Recursion over iterative algorithms are:
- Adds clarity or better readability of code.

### How
It calls itself for a smaller input.

### What
Recursion is a type of algorithm that calls itself for the same nature of problem on a smaller test case. 

**Example:**
```c++
// Calculting factorial using Recursion
int factorial(int n)
{
	// Base Case
	if(n==0)
		return 1;
	// Function calling itself below:
	int small = factorial(n-1);
	return n = small;	
}

int main()
{
	int n;
	cin >> n;
	int output = factorial(n);
	cout << output;
}
```
