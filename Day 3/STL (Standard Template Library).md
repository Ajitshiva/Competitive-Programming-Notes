1. vector
2. set
3. multiset
4. map
5. multimap
6. unordered_set
7. unordered_map
8. deque
9. stack
10. queue
11. string

### Vector

```cpp
	vector<int> arr;
	arr.push_back(1); // add 1 to arr // TC: O(1)
	arr.pop_back(); // remove last element added to arr // TC: O(1)
	cout << arr.size() << '\n'; // print size of arr 
	cout << arr.back() << '\n'; // print last element of arr
	vector<int> arr1(5);
	cout << arr1.size() << '\n'; // 5'
	vector<int> arr2(5, 5);
	for(int i : arr1) {
		cout << i << ' ';
	}
	cout << '\n';
	vector<vector<int>> vec2d(5, vector<int>(3));
	for(auto it : vec2d) {
		for(int i : it) {
			cout << i << ' ';
		}
		cout << '\n';
	}
	cout << '\n';
	vector<vector<vector<int>>> vec3d(5, vector<vector<int>>(4, vector<int>(3)));
	for(auto it : vec3d) {
		for(auto it1 : it) {
			for(int i : it1) {
				cout << i << ' ';
			}
			cout << '\n';
		}
		cout << '\n';
	}
```

### Set:

```cpp
	set<int> s; // set will maintain sorting order and remove duplicate numbers
	s.insert(5); // add element to s TC: O(logN)
	s.count(5); // number of occurence of 5 present in the set TC: O(logN)
	s.erase(5); // remove element 5 from the set O(logN)
	s.size(); // return size of the set TC: O(1)
	s.empty(); // given set is empty TC: O(1)
	auto it = s.lower_bound(5); // first element which is atleast 5 TC: O(logN)
	vector<int> vec = {5, 4, 3, 3, 2};
	set<int> s1(vec.begin(), vec.end()); // convert vector to set
	for(int i : s1) {
		cout << i << '\n';
	}
	/* Output:-
		2
		3
		4
		5
	*/
```

### Multiset:

```cpp
	multiset<int> ms; // multiset will maintain sorting order and won't remove duplicate numbers
	ms.insert(5);
	ms.insert(5);
	// ms.erase(5); // remove all element whose values is 5
	ms.erase(ms.find(5));
	cout << ms.count(5) << '\n'; // return 1
	for(int i : ms) {
		cout << i << ' ';
	}
	cout << '\n';
	/*
	Output:
	1
	5 
	*/
```

### Map:

```cpp
	map<string, int> mp;
	mp["ajit"] = 4;
	mp["karthick"] = 5;

	for(auto it : mp) {
		cout << it.first << ' ' << it.second << '\n';
	}
	// Output:
	// ajit 4
	// karthick 5
```

### Multimap:

```cpp
	multimap<string, int> mmp;
	mmp.insert({"ajit", 4});
	mmp.insert({"ajit", 5});
	for(auto it : mmp) {
		cout << it.first << ' ' << it.second << '\n';
	}
	// Output:
	// ajit 4
	// ajit 5
```