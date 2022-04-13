# 4. Recursion and Arrays
Check if the array is sorted using a Recursive Algorithm: 

```c++
bool sort(int a[], int size)
{
    if(size==0 || size==1)
        return true;

    if(a[0]>a[1])
        return false;
  
    bool small = sort(a+1, size-1);
    return small;
}

int main()
{
    int a[5]={1,0,3,4,5};
    int size = 5;
    cout << sort(a,5);
}
```

![](Pasted%20image%2020220413030056.png)