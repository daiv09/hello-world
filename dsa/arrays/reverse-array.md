# Reverse an Array

### Approach 1

```
int arr[n];
for(int i=n-1;i>-1;i--)
    print(arr[i])
```

Time Complexity \
TC-> O(n) \
SC-> O(n) \
Auxillary Space-> O(1)

---

### Approach 2


```
int arr[n];
int s=0,e=n-1;
while(s<=e){
    temp=arr[s];
    arr[s]=arr[e];
    arr[e]=temp;
    s++;
    e--;
}
```

TC-> O(n/2) \
SC-> O(n) \
Auxillary Space-> O(1)