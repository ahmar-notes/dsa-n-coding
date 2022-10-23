# 6. Inline and default arguments

## Inline
### Why
Inline has same advantages as Macros, but for functions. But it can only works for 2-3 line of function's code, or compiler dependent.

### How
Write `inline` keyword before making the function.

```c++
inline return_type function_name(){}
```

## Default arguments
### Why
Sometimes a function can have no specific arguments, but we cannot leave the argument empty, instead we can declare default arguments to take place if no value provided. 

### How
Default values can be defined as:
```c++
//Example
int max(int a, int b = 0)
```

**Note:** Place all default arguments on the rightmost side. Reason: Not doing so creates ambiguity for the compiler.