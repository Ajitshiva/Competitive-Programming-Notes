
```cpp
	int arr[n];
	vector<int> vec(n);
	vector<vector<int>> vec_2d(n);
	sort(arr, arr + n); // sort the array asc
	sort(arr.begin(), arr.end()); // sort the vector asc
	sort(arr.rbegin(), arr.rend()); // sort the vector desc
	sort(arr.begin(), arr.end(), [](int a, int b) {
		return b < a; // sort the vector desc
	}); 
	sort(arr.begin(), arr.end(), [](vector<int> a, vector<int> b) {
		return a[1] < b[1]; // sort the 2d vector by second element asc 
	});

	// TC : O(nlogn)
	
```


[2545: Sort the Students by Their Kth Score:](https://leetcode.com/problems/sort-the-students-by-their-kth-score/description/) 

There is a class with `m` students and `n` exams. You are given a **0-indexed** `m x n` integer matrix `score`, where each row represents one student and `score[i][j]` denotes the score the `ith` student got in the `jth` exam. The matrix `score` contains **distinct** integers only.

You are also given an integer `k`. Sort the students (i.e., the rows of the matrix) by their scores in the `kth` (**0-indexed**) exam from the highest to the lowest.

Return _the matrix after sorting it.

```
**Input:** score = [[10,6,9,1],[7,5,11,2],[4,8,3,15]], k = 2
**Output:** [[7,5,11,2],[10,6,9,1],[4,8,3,15]]
**Explanation:** In the above diagram, S denotes the student, while E denotes the exam.
- The student with index 1 scored 11 in exam 2, which is the highest score, so they got first place.
- The student with index 0 scored 9 in exam 2, which is the second highest score, so they got second place.
- The student with index 2 scored 3 in exam 2, which is the lowest score, so they got third place.
- 
```


Solution in CPP:

```cpp
class Solution {
	public:
	vector<vector<int>> sortTheStudents(vector<vector<int>>& arr, int k) {
		sort(arr.begin(), arr.end(), [&](vector<int>& a, vector<int>& b) {
			return b[k] < a[k]; // sort the 2d vector by kth element desc
		});
	return arr;
	}
};
```



