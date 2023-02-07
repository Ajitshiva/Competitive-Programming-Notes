```
	for(int i = 0; i < n; i++) {
		// N times this code will execute
		// TC : O(N)
	}
	

	for(int i = 0; i < n; i++) {
		for(int j = 0; j < n; j++) {
			// N * N times this code will execute
			// TC : O(N^2)
		}
	}

	

	for(int i = 0; i < n + 10; i++) {
		// TC : O(N)
	}
	

	for(int i = 0; i < n; i++) {
		for(int j = i; j < n; j++) {
			// N + (N - 1) + (N - 2) .... 0
			//1 + 2 + 3 + ... n = n (n + 1) / 2
			//n^2 + n / 2
			// TC : O(N^2)
		}
	}

	

	for(int i = 0; i < n; i++) {
		for(int j = 0; j < m; j++) {
			// TC : O(NM)
		}
	}

	

	
```