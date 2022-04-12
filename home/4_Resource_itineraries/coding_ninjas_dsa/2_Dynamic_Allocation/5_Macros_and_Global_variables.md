# 5. Macros and Global variables
## Macros
### Why
Macros are used for two reasons:
1. They decrease memory, time costs due to extra variables.
2. They help reduce verbosity(ugly and long) of code by replacing long lines of code by an intuitive name.

Macros are nothing but code that are replaced by the pre-processor before the compilation step. See this:
![](Preprocessor-In-C.png)

### How
- The `#define` preprocessor directive is used to define macros and their value.
- The syntax is:
```c++
#define replacement value

// example
#define PI 3.14
```

---
## Global variable
Using them is a **bad practice** because they are easy to change and have an absurdly high impact of change.