1. `lower_bound`  returns a pointer to the first array element whose value is atleast x
2. `upper_bound` returns a pointer to the first array element whose value is larger than x
3. `equal_range` return both above pointers

```cpp
	int arr[] = {1, 2, 2, 3, 3, 4, 5};
	int n = sizeof(arr) / sizeof(arr[0]);
	int k = lower_bound(arr, arr + n, 3) - arr; // 3 
	int k1 = upper_bound(arr, arr + n, 3) - arr; // 5



	// Find the number of occurence of given number present in the given array
	int count = upper_bound(arr, arr + n, 3) - lower_bound(arr, arr + n, 3); // 2


	auto count1 = equal_range(arr, arr + n, 3);
	// equal_range return both lower_bound pointer and upper_bound pointer
	cout << count1.second - count1.first << '\n'; // 2
```


```cpp
int lower_bound(int x, vector<int>& arr) {
	        // x-1 x x+1
	// F F F F T T T T T T
	// low always lies in F
	// high always  lies in T 
	int n = arr.size();
	int low = -1, high = n - 1;
	while(low + 1 < high) {
		int mid = low + (high - low) / 2;
		if(arr[mid] >= x) {
			high = mid;
		} else { // arr[mid] < x
			low = mid;
		}
	} 
	return high;
}

int upper_bound(int x, vector<int>& arr) {
	        // x-1 x x+1
	// F F F F T T T T T T
	// 
	// low always lies in F
	// high always  lies in T 
	int n = arr.size();
	int low = -1, high = n;
	while(low + 1 < high) {
		int mid = low + (high - low) / 2;
		if(arr[mid] > x) {
			high = mid;
		} else { // arr[mid] < x
			low = mid;
		}
	} 
	return high;
}
```

