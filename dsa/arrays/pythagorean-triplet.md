# Pythagorean Triplet

```cpp
int arr[n];
for(int i=0;i<n;i++)
    for(int j=i+1;j<n;j++)
        for(int k=j+1;k<n;k++)
            if(arr[i]*arr[i]+arr[j]*arr[j]==arr[k]*arr[k] ||
            arr[j]*arr[j]+arr[k]*arr[k]==arr[i]*arr[i] ||
            arr[k]*arr[k]+arr[i]*arr[i]==arr[j]*arr[j] ||)
                return true;
return false;
```

TC-> O(n^3)