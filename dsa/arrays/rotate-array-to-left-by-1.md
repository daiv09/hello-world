# 🌟 Rotating an Array in C++ 🌟

## 📌 Problem Statement
Given an array of size `n`, we need to rotate its elements by one position. This can be done either to the right or to the left.

---

## ✅ Rotating Right by One
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

## ✅ Rotating Left by One
### 📝 Code:
```cpp
#include <iostream>
using namespace std;

void rotateLeftByOne(int arr[], int n) {
    int temp = arr[0]; // Store the first element
    
    for(int i = 0; i < n-1; i++) {
        arr[i] = arr[i+1]; // Shift elements to the left
    }
    arr[n-1] = temp; // Move first element to the last position
}

int main() {
    int arr[] = {2, 3, 4, 5, 6, 7};
    int n = sizeof(arr) / sizeof(arr[0]);

    rotateLeftByOne(arr, n);

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
### 🔄 Right Rotation:
1. **Store Last Element:** 
   - The last element (`arr[n-1]`) is stored in `temp`.
2. **Shift Elements Right:** 
   - The loop iterates **from right to left** (`i = n-1` to `i >= 1`), shifting elements one position to the right.
3. **Place Stored Element at First Position:** 
   - Assign `temp` to `arr[0]` to complete the rotation.

### 🔄 Left Rotation:
1. **Store First Element:** 
   - The first element (`arr[0]`) is stored in `temp`.
2. **Shift Elements Left:** 
   - The loop iterates **from left to right** (`i = 0` to `i < n-1`), shifting elements one position to the left.
3. **Place Stored Element at Last Position:** 
   - Assign `temp` to `arr[n-1]` to complete the rotation.

---

## 🕑 Complexity Analysis:
- **Time Complexity:** \(O(n)\), since we traverse the array once.
- **Space Complexity:** \(O(1)\), as we only use a temporary variable.

---

## 🎯 Output Example:
### 🔄 Right Rotation Output:
```
7 2 3 4 5 6
```
### 🔄 Left Rotation Output:
```
3 4 5 6 7 2
```

This method ensures that the array is correctly rotated by one position in both directions. 🚀

