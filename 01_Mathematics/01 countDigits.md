## Problem:
* Find out the number of digit in a number.
* Input : 23456
* Output : 5

### Logic:
#### BruteForce Approach
* run a loop till number > 0.
* divide the number by 10.
* increse the counter variable every time.


### Code:
```cpp
#include <iostream>
using namespace std;

int countDigit(int x) {
	int cnt = 0;

	while(x>0) {
		x = x / 10;
		cnt += 1;
	}
	return cnt;
}
int main() {
  int  num;
	cin >> num;

	int res = countDigit(num);

	cout << res << endl;
}
```
