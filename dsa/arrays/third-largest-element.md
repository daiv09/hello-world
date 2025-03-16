# Third Largest Element in the Array

## Case 1:
```cpp
int arr[n];
// sort the array
int thirdMax=arr[n-3];
```

```cpp
int arr[n];
// sort the array
int max=arr[n-1],secMax=arr[n-2],thirdMax=0;
for(int i=n-1;i>=0;i--){
    if(arr[i]!=max && arr[i]!=secMax)
        thirdMax=arr[i];
}
```

## Case 2:
```cpp
int max=INT_MIN,secMax=-1,thirdMax=0;
for(int i=0;i<n;i++)
    if(arr[i]>max)
        max=arr[i];
    
for(int i=0;i<n;i++)
    if(arr[i]>secMax && arr[i]!=max)
        secMax=arr[i];

for(int i=0;i<n;i++)
    if(arr[i]>thirdMax && arr[i]!=max && arr[i]!=secMax)
        thirdMax=arr[i];
```

## Optimal Approach

```cpp
int max=INT_MIN,secMax=-1,thirdMax=0;
for(int i=0;i<n;i++){
    if(arr[i]>max){
        thirdMax=secMax;
        secMax=max;
        max=arr[i];
    }
    else if(arr[i]>secMax){
        thirdMax=secMax;
        secMax=arr[i];
    }
    else if(arr[i]>thirdMax)
}
```