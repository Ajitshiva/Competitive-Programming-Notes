1. Linear Search
2. Binary Search

#### Linear Search

Algorithm:

	We have to scan the each element and check if the element is present or not

Code:

```cpp
	bool flag = false;
	for(int i = 0; i < n; i++) {
		if(arr[i] == target) {
			flag = true;
		}
	}
	if(flag) {
		cout << target << "is present in the given array" << '\n';
	} else {
		cout << target << "is not present in the given array" << '\n';
	}
```

Time complexity: $O(N)$ where $N$ is size of the array

#### Binary Search:

Algorithm:

	We have to check the mid element 
	if the mid element is equal to target, then we have to stop the algorithm 
	if the mid element is greater than the target, then we have to update r = mid - 1
	if the mid element is less than the target, then we have to update l = mid + 1

Code:

```cpp
	bool flag = false;
	int low = 0, high = n - 1;
	while(low <= high) {
		int mid = low + (high - low) / 2; // (low + high) // 2
		if(arr[mid] == target) {
			flag = true;
		} else if(arr[mid] < target) {
			r = mid - 1;
		} else { // arr[mid] > target
			l = mid + 1;
		}
	}
	if(flag) {
		cout << target << "is present in the given array" << '\n';
	} else {
		cout << target << "is not present in the given array" << '\n';
	}
```

Time Complexity: $O(logN)$ where $N$ is size of the array

Problem Link:
- [704. Binary Search](https://leetcode.com/problems/binary-search/description/)
- [69. Sqrt(x)](https://leetcode.com/problems/sqrtx/)
```cpp

int mySqrt(int x) {
	// T T T T T F F F F F
	// We have to find the last T in this sequence
	// l always lies in T
	// r always lies in F
	long long int l = 0, r = x + 1;
	while(l + 1 < r) {
		long long int mid = l + (r - l) / 2;
		if(mid * 1LL * mid <= x) {
			l = mid;
		} else {
			r = mid;	
		}
	}
	return l;
}
	
	
```







