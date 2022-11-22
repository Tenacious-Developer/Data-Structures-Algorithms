## Count Set Bits
* number of bit 1 
```
n = 15 = 0000 1111 = 4 
cnt = 0
n & 1 = 1111
           1
     ----------
            1
     ----------
 store the result of 1 in cnt variable and right shift the bit and again repeat the loop
 ```
 ```cpp
#include <iostream>
using namespace std;

int countSetBits(int n){
	int cnt = 0;
	while(n>0){
		int last_bits = (n & 1);
		cnt += last_bits;
		n = n >> 1;
	}
	return cnt;
}

int main() {
  int n;
  cin >> n;

  cout << countSetBits(n) << endl;


  return 0;
}
```
### Fater method
*  removes the last bit in each iteration
```
n   = 15  = 1111
n-1 = 14  = 1110
n = n & (n-1) = 1110 = 14
again 
n   = 14  = 1110
n-1 = 13  = 1101
n & (n-1) = 1100 = 12
```
```cpp
#include <iostream>
using namespace std;

int countSetBitsHeck(int n){
	int ans = 0;
	while(n>0){
		// removes the last bit in each iteration
		n = n & (n-1);
		ans++;
	}
	return ans;
}

int main() {
  int n;
  cin >> n;

  cout << countSetBitsHeck(n) << endl;

  return 0;
}
```
