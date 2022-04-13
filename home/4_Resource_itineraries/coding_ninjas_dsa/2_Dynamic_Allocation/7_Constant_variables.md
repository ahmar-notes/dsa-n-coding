# 7. Constant variables

### Why
- It's most important reason is to avoid bugs.
- Constant variable allow the compiler to catch any attempts to change it.

### How
To make a variable constant `const` keyword is used:

**Syntax:**
```c++
	const data_type variable_name = value;
```

**Note:** A constant variable must be initialize on the point of declaration.

### What
A constant variable is a type of variable whose value cannot be reassigned directly. This is used to avoid the chance of making error by unintentionally changing the value of variable.
But if we willing want to change/alter the value of the constant variable, we can do that by changing the value by accessing the memory location of that variable. As:

```c++
int i =10;
int const *p = &i;
i++;
```

As above, the path to the variable is fixed via p. But the variable can be still altered through the main variable. (Can also be done with reference variable)
