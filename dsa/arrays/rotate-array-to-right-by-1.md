# 🌟 Rotating an Array to the Right by 1 in C++ 🌟

## 📌 Problem Statement
Given an array of size `n`, we need to rotate its elements to the right by one position. This means that the last element of the array should become the first, and all other elements should shift one position to the right.

---

## ✅ Correct Implementation
### 📝 Code:
```cpp
#include <iostream>
using namespace std;

void rotateRightByOne(int arr[], int n) {
    int temp = arr[n-1]; // Store the last element
    
    for(int i = n-1; i >= 1; i--) {
        arr[i] = arr[i-1]; // Shift elements to the right
    }
    arr[0] = temp; // Move last element to the first position
}

int main() {
    int arr[] = {2, 3, 4, 5, 6, 7};
    int n = sizeof(arr) / sizeof(arr[0]);

    rotateRightByOne(arr, n);

    // Print the rotated array
    for(int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
    
    return 0;
}
```

---

## 📖 Explanation:
1. **Store Last Element:** 
   - The last element (`arr[n-1]`) is stored in `temp`.

2. **Shift Elements Right:** 
   - The loop iterates **from right to left** (`i = n-1` to `i >= 1`), shifting elements one position to the right.

3. **Place Stored Element at First Position:** 
   - Assign `temp` to `arr[0]` to complete the rotation.

---

## 🕑 Complexity Analysis:
- **Time Complexity:** \(O(n)\), since we traverse the array once.
- **Space Complexity:** \(O(1)\), as we only use a temporary variable.

---

## 🎯 Output Example:
```
7 2 3 4 5 6
```

This method ensures that the array is correctly rotated to the right by one position. 🚀

