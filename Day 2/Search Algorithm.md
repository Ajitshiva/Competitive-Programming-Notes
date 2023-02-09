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

