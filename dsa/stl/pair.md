# Pair

```cpp
#include<iostream>
#include<utility>
using namespace std;

int main(){
    /*
        Pairs included in utility header file
    */
    pair<int, int> p1={1,2};
    cout<<p1.first<<" "<<p1.second;
    
    cout<<endl;
    
    pair<int, pair<int, char>> p2={1,{1,'a'}};
    cout<<p2.first<<" "<<p2.second.second;
    
    cout<<endl;
    
    pair<int, int> p3[]={{1,2},{3,4},{5,6},{7,8},{9,10}};
    cout<<p3[1].first;
    return 0;
}
```