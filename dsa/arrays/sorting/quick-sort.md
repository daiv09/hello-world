# Quick Sort

```cpp
void quickSort(int l,int h,int arr[]){
    partition=partition(l,h,arr[]);
    quickSort(l,partition-1,arr[]);
    quickSort(partition+1,h,arr[]);
}

int partition(int l,int h,int arr[]){
    
}
```