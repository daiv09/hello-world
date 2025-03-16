# Check whether an Array is sorted or not

```cpp
int arr[n];
for(int i=0;i<n-1;i++)
    if(arr[i]>arr[i+1])
        return false;
return true;
```