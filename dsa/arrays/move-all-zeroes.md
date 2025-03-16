# Moving all Zeroes to the end of the array

## Brute Approach

```cpp
int arr[n];
vector<int> v;
for(int i=0;i<n;i++)
    if(arr[i]!=0)
        v.push_back(arr[i]);
for(int i=0;i<v.size();i++)
    arr[i]=v[i];
for(int i=v.size();i<n;i++)
    arr[i]=0;
```

### Time Complexity
TC-> O(n+non-zero-elements+(n-non-zero-elements))
  -> O(2n)

SC-> O(n)

## Optimal Approach

Two Pointer Approach
```cpp

```