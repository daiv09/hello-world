# Merge Sort

```cpp
void mergeSort(int l,int h,int arr[]){
    mid=l+(h-l)/2;
    mergeSort(l,mid-1,arr[]);
    mergeSort(mid,h,arr[]);
    merge(l,mid,h,arr[]);
}

int merge(int l,int mid,int h,int arr[]){
    
}
```