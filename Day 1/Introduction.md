### C++ Code Template

```cpp
#include<bits/stdc++.h>
using namespace std;

int main() {
	// solution comes here
}
```

### Input and Output

```cpp
	int a, b, c;
	string s;
	cin >> s;
	cout << s; // read string
	getline(cin, s); // read whole line
	cin >> a >> b >> c; // read integers
	cout << a + b + c;
```

### Fast I/O

```cpp
	ios::sync_with_stdio(0);
	cin.tie(0);
```

### Read Unlimited data

```cpp
	int x;
	while(cin >> x) {
		cout << x << endl;
	}
```

### Read Large Values Around 10^18

```cpp
	long long int x;
```

### Print Decimal Values upto 6 Decimals
```cpp
	float pi = 3.1415;
	cout << fixed << setprecision(6) << pi << '\n';
```

``Use \n instead of endl``

### Mathematics:

Sum of the first $N$ Natural numbers = $n * (n + 1) / 2$
Sum of the first $N$ Squares of Numbers = $(n * (n + 1) * (2n + 1)) / 6$

#### Find Factorial:
```cpp
	int findFactorial(int n) {
		if(n == 1) return 1;
		return n * findFactorial(n  - 1);
	}
```

### Logarithms:

Logb(x) is equals of number of times we have to divide x by b until reach 1

```
8/2 = 4
4/2 = 2
2/2 = 1
Log(8) = 3
```

- $log_b(a * b) = log_b(a) + log_b(b)$
ex :- $log(10) = log(5) + lob(2)$
- $log_b(a^b) = blog_b(a)$
- $log_b(a / b) = log_b(a) - log_b(b)$

### CP Links:

- [Codeforces](https://codeforces.com/)
- [Codechef](https://www.codechef.com/)
- [Atcoder](https://atcoder.jp/)





