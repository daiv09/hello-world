# Vector

## Dynamic Arrays

```cpp
#include<iostream>
#include<vector>
using namespace std;
int main(){
    vector<int> v1;
    vector<int> v2={1,2,3,4,5};
    vector<int> v3(5,-1);

    for(auto it: v2)
        cout<<it<<endl;

    return 0;
}
```