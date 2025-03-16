# Selection Sort

```cpp
int arr[n];
for(int i=0;i<n-1;i++){
    int minpos=i;
    for(int j=i+1;j<n;j++)
        if(arr[j]<arr[minpos])
            minpos=j;
    if(minpos!=i)
        swap(arr[i],arr[minpos]);
}
```