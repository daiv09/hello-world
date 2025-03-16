# Second Largest Element in the Array

### Case 1:  All **distinct** elements

```
int arr[n];
// sort the array
print(arr[n-1]); // maximum
print(arr[n-2]); // second maximum

```

### Time Complexity

TC-> O(n logn) + O(1)
TC-> O(n logn)

---

### Case 2:  Not all distinct elements


```
int arr[n];
// sort the array
max=arr[n-1]; // maximum

for(int i=n-1; i>-1; i--){
    if(arr[i]!=max){
        secMax=arr[i];
    }
}

```

### Time Complexity

TC-> O(n logn) + O(n)\
TC-> O(n logn)

---

### Case 3: Optimal Approach

```cpp
int max=INT_MIN,secMax=0;
for(int i=0;i<n;i++){
    if(arr[i]>max){
        arr[secMax]=max;
        max=arr[i];
    }
    else if(arr[i]>arr[secMax])
        arr[secMax]=arr[i];
}
```