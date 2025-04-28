# Sieve of Eratosthenes

### Find all prime numbers up to a given number `n`

The **Sieve of Eratosthenes** is an efficient algorithm to find all prime numbers up to a given number `n`.  
It works by marking the multiples of each prime number starting from 2.

Below is the C++ implementation:

```cpp
#include<iostream>
using namespace std;

void sieve(int n){
    int arr[n+1];
    
    // Initialize all entries as 1 (true)
    for(int i = 0; i <= n; i++){
        arr[i] = 1;
    }

    arr[0] = arr[1] = 0; // 0 and 1 are not prime

    for(int i = 2; i * i <= n; i++){
        if(arr[i]){
            for(int j = i * i; j <= n; j += i){
                arr[j] = 0;
            }
        }
    }

    // Print all prime numbers
    for(int i = 2; i <= n; i++){
        if(arr[i]){
            cout << i << " ";
        }
    }
}

int main(){
    int n;
    cin >> n;
    sieve(n);
    return 0;
}
