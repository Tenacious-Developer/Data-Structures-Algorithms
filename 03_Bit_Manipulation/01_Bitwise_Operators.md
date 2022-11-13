## Binary And(&)
### Rules
* if any one bit is 0 then result will be 0
```
0 & 0 = 0
0 & 1 = 0
1 & 0 = 0
1 & 1 = 1
```
* Example
```
5 = 0101
6 = 0110
5 & 6 = 0101
        0110
      -------
        0100    =  4
```
```cpp
#include <iostream>
using namespace std;

int main() {
  int a = 5;
  int b = 6;
  int c = a & b;

  cout << c << endl; // 4
}
```
## Binary OR(|)
### Rules
* if any one bit is 1 then result will be 1
```
0 & 0 = 0
0 & 1 = 1
1 & 0 = 1
1 & 1 = 1
```
* Example
```
5 = 0101
6 = 0110
5 & 6 = 0101
        0110
      -------
        0111    =  7
```
```cpp
#include <iostream>
using namespace std;

int main() {
  int a = 5;
  int b = 6;
  int c = a | b;
  cout << c << endl; // 7
}
```
## Binary XOR(^)
### Rules
* if both bit is same then result is 0
```
0 ^ 0 = 0
0 ^ 1 = 1
1 ^ 0 = 1
1 ^ 1 = 0
```
* Example
```
5 = 0101
6 = 0110
5 ^ 6 = 0101
        0110
      -------
        0011    =  3
```
```cpp
#include <iostream>
using namespace std;

int main() {
  int a = 5;
  int b = 6;
  int c = a ^ b;
  cout << c << endl; // 3
}
```
