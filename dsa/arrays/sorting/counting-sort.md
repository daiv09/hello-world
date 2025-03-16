# Counting Sort

```cpp
int arr[n],max=INT_MIN;
for(int i=0;i<n;i++)
    if(arr[i]>max)
        max=arr[i];
    
int count[max+1]={0};
for(int i=0;i<n;i++)
    ++count[arr[i]];

for(int i=1;i<max+1;i++){
    count[i]=count[i-1];
}


```