C++ Code Template

```
#include<bits/stdc++.h>
using namespace std;

int main() {
	// solution comes here
}
```

Input and Output

```
	int a, b, c;
	string s;
	cin >> s;
	cout << s; // read string
	getline(cin, s); // read whole line
	cin >> a >> b >> c; // read integers
	cout << a + b + c;
```

Fast I/O

```
	ios::sync_with_stdio(0);
	cin.tie(0);
```

Read Unlimited data

```
	int x;
	while(cin >> x) {
		cout << x << endl;
	}
```

Read Large Values Upto 10^18

```
	long long int x;
```

Print Decimal Values upto 6 Decimals
```
	float pi = 3.1415;
	cout << fixed << setprecision(6) << pi << '\n';
```

``Use \n instead of endl``

Mathematics:

Sum of N Natural numbers = n * (n + 1) / 2
Sum of N Squares of Numbers = (n * (n + 1) * (2n + 1)) / 6

Find Factorial:
```
	int findFactorial(int n) {
		if(n == 1) return 1;
		return n * findFactorial(n  - 1);
	}
```

Logarithms:

Logb(x) is equals of number of times we have to divide x by b until reach 1

```
8/2 = 4
4/2 = 2
2/2 = 1
Log2(8) = 3
```

- logb(a * b) = logb(a) + logb(b)
ex :- log(10) = log(5) + lob(2)
- logb(a^b) = blogb(a)
- logb(a / b) = logb(a) - logb(b)

CP Links:

https://codeforces.com/
https://www.codechef.com/
https://atcoder.jp/





