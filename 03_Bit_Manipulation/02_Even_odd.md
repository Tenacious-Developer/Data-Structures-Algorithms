* if last bit = 1 then odd
* if last bit = 0 then even
#### Example
```
5 = 0101 (odd, last digit is 1)
6 = 0110 (even, last digit is 0)
```
* To find even and odd, perform and(&) operation with a number
#### Example
```
5   = 0101
5&1 = 0101
      0001
    --------
      0001   last bit is 1, odd
```
```
6   = 0110
5&1 = 0110
      0001
    --------
      0000   last bit is 0, even
```
### Pseudocode
```
if(x&1){
	cout << "odd" << endl;
}else{
	cout << "even" << endl;
}
```
### CPP
```cpp
#include <iostream>
using namespace std;

int main() {
  int x;
	cin >> x;

	if(x&1){
		cout << "odd" << endl;
	}else{
		cout << "even" << endl;
	}
	
	return 0;
}
```
