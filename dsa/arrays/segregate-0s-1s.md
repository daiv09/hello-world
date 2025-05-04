# Segregate 0's and 1's 

```cpp
#include <iostream>
#include <algorithm>
using namespace std;

void app1(int arr[], int n){
    for(int i=0;i<n;i++)
        cout<<arr[i]<<" ";
    
    cout<<"\n";
    
    sort(arr,arr+n);
    for(int i=0;i<n;i++)
        cout<<arr[i]<<" ";
}
void app2(int arr[], int n){
    int ctr0,ctr1;
    ctr0=ctr1=0;
    for(int i=0;i<n;i++){
        if(arr[i]==0)
            ctr0++;
        else ctr1++;
    }
    
    for(int i=0;i<ctr0;i++){
        arr[i]=0;
    }
    for(int i=ctr0;i<ctr0+ctr1;i++){
        arr[i]=1;
    }
    
    cout<<"\n";
    
    for(int i=0;i<n;i++)
        cout<<arr[i]<<" ";
}
void app3(int arr[], int n){
    int l=0,r=n-1;
    while(l<r){
        if(arr[l]==0)
            l++;
        if(arr[r])
            r--;
        if(arr[l]>arr[r]){
            swap(arr[l],arr[r]);
            l++;
            r--;
        }
    }
    
    cout<<"\n";
    
    for(int i=0;i<n;i++)
        cout<<arr[i]<<" ";
}

int main() {
    int arr[]={1,0,1,0,0,0,1,0};
    int n=(sizeof(arr)/sizeof(arr[0]));
    app1(arr,n);
    app2(arr,n);
    app3(arr,n);
    return 0;
}
```