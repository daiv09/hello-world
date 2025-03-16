# 📌 Euclidean Algorithm for GCD

## 📝 Explanation:
The Euclidean algorithm states that the **Greatest Common Divisor (GCD)** of two numbers `a` and `b` is equal to `gcd(a-b, b)` when `a > b`, which simplifies to `gcd(a % b, b)`.

## ✅ Code Implementation:
```cpp
#include <iostream>
using namespace std;

int gcd(int m, int n) {
    while(n != 0) {
        int mod = m % n;
        m = n;
        n = mod;
    }
    return m;
}

int main() {
    int a, b;
    cout << "Enter two numbers: ";
    cin >> a >> b;
    cout << "GCD of " << a << " and " << b << " is: " << gcd(a, b) << endl;
    return 0;
}
