
```cpp
    // O(N^3) solution for finding max_subarray_sum
	for(int i = 0; i < n; i++) {
		for(int j = i; j < n; j++) {
			int sum = 0;
			for(int k = i; k <= j; k++) {
				sum += arr[k];
			}
			global_sum = max(global_sum, sum);
		}
	}

	// O(N^2) solution for finding max_subarray_sum
	for(int i = 0; i < n; i++) {
		for(int j = i; j < n; j++) {
			int sum = pref[j]; // where pref[i] is sum of first i number in array
			if(i != 0) sum -= pref[i - 1];
			global_sum = max(global_sum, sum);
		}
	}

	// O(N) solution for finding max_subarray_sum
	int curr_sum = 0, global_sum = INT_MIN;
	for(int i = 0; i < n; i++) {
		// check  whether arr[i] is profit to the existed sum or not
		curr_sum = max(arr[i], curr_sum + arr[i]); 
		global_sum = max(curr_sum, global_sum);
	}
```

