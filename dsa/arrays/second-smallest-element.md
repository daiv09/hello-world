# Second Smallest Element in the Array

### Case 1:  All **distinct** elements

```
int arr[n];
// sort the array
print(arr[0]); // minimum
print(arr[1]); // second minimum

```

### Time Complexity

TC-> O(n logn) + O(1)
TC-> O(n logn)

---

### Case 2:  Not all distinct elements


```
int arr[n];
// sort the array
min=arr[0]; // min

for(int i=0; i<n>; i++){
    if(arr[i]!=min){
        secMin=arr[i];
    }
}

```

### Time Complexity

TC-> O(n logn) + O(n)
TC-> O(n logn)

---

### Case 3: Optimal Approach

```cpp
int min=INT_MAX,secMin=arr[0];
for(int i=0;i<n;i++){
    if(arr[i]<min){
        secMin=min;
        min=arr[i];
    }
    else if(secMin>arr[i])
        secMin=arr[i]
}
```