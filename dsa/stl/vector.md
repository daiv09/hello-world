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
    vector<pair<int, int>> v4={{2,3}};
    vector<int> v5(5);
    vector<int> v6(v5);

    for(auto it: v3)
        cout<<it<<endl;

    cout<<endl;
    
    v1.push_back(10);
    v1.emplace_back(5);
    
    
    v1.push_back(10);
    v1.emplace_back(5);
    
    for(auto it: v1)
        cout<<it<<endl;
    
    // Difference between push_back() and emplace_back()
    // emplace_back() is faster 
    // In case of pairs 
    
    v4.push_back({5,7});
    v4.emplace_back(11,13);
    
    vector<pair<int, int>>::iterator it=v4.begin();
    for( ;it!=v4.end();it++){
        cout<<it->first<<"-->"<<it->second<<endl;
    }
    
    cout<<endl;
    
    for(auto it: v5)
        cout<<it<<endl;
    
    cout<<endl;
    
    cout<<v2[0]<<endl;
    cout<<v2.at(1)<<endl;
    cout<<v2.back()<<endl;
    cout<<v2.size()<<endl;
    cout<<v2.capacity()<<endl;
    
    // .erase(it)
    // .erase(st,end+1)
    
    
    cout<<endl;
    
    for(auto it=v2.begin();it!=v2.end();it++){
        cout<<*it<<" ";
    }
    v2.erase(v2.begin());
    
    cout<<endl<<v2.at(0)<<endl;
    v2.erase(v2.begin(),v2.end()-1);
    cout<<endl<<v2.at(0)<<endl;
    
    return 0;
}
```