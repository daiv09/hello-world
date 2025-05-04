# Sort an array of 0's, 1's and 2's

## Brute Force Solution
```cpp
// sorting the array
```
TC-> O(nlogn)

## Better Solution
```cpp
int c0=0,c1=0,c2=0;
for(int i=0;i<n;i++){
    if(arr[i]==0)   c0++;
    if(arr[i]==1)   c1++;
    if(arr[i]==2)   c2++;
}
for(int i=0;i<c0;i++)   arr[i]=0;
for(int i=c0;i<c0+c1;i++)   arr[i]=1;
for(int i=c0+c1;i<n;i++)   arr[i]=2;
```
TC-> O(n+n)

## Optimal Solution - **Dutch National Flag Algortihm**

```cpp
int arr[n];
int low=0,mid=0,high=n-1;
while(mid<=high){
    if(arr[mid]==0)
        swap(arr[low],arr[mid])
        low++;  mid++;
    else if(arr[mid]==1)
        mid++;
    else
        swap(arr[mid],arr[high])
        high--;
}
```