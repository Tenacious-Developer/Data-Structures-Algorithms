## Clear bits in range:
```
int n = 31 => 0000 0001 1111 after clear bits in range of 2 to 4 it becomes 0000 0000 0011
int n = 0000 0001 1111
int a = (~0) << (j+1) i.e j = 5 => 1111 1110 0000
int b = ( 1 << i ) - 1 => 4 -1 = 3 => 0000 0000 0011
mask = a | b = 1111 1110 0011
n & mask = 0000 0001 1111
           1111 1110 0011
				---------------------
           0000 0000 0011   =  3
```
### Pseudocode
```
void clearBitsInRange(int n, int i, int j){
	int a = (~0) << (j+1);
	int b = (1 << i) - 1;
	int mask = (a | b);
	int res = (n & mask);
	cout << res << endl;
}
```
### CPP
```cpp
#include <iostream>
using namespace std;

void clearBitsInRange(int n, int i, int j){
	int a = (~0) << (j+1);
	int b = (1 << i) - 1;
	int mask = (a | b);
	int res = (n & mask);
	cout << res << endl;
}

int main() {
	int n = 31;
	int i = 2;
	int j = 4;

	clearBitsInRange(n, i, j);
	return 0;
}
```
### Example Question 
```
N = 10000000000
M = 10101
i = 2
j = 6
put m in the range of i to j
```
```cpp
#include <iostream>
using namespace std;

void clearBitsInRange(int &n, int i, int j){
	int a = (~0) << (j+1);
	int b = (1 << i) - 1;
	int mask = (a | b);
	int res = (n & mask);
}
void replaceBits(int &n, int i, int j){
	clearBitsInRange(n,i,j);
  int mask = (m << i);
  int n = n | mask;
}
int main() {
	int n = 10000000000;
  int m = 10101
	int i = 2;
	int j = 6;

	replaceBits(n, i, j);
	return 0;
}
```
