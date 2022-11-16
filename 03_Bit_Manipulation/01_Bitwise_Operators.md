## Binary And(&)
### Rules
* if both bit is 1 then the result will be 1
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
* if both bit is different then result will be 1
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
## Binary NOT(~ )
### Rules
* it does inversion of all the bit
```
~ 0 = 1
~ 1 = 0
```
* Example
```
x = 6 => 28 leading zeros 0000 and 0110
~x = 28 leading 1111 and 1001 and msb shows the sign (-ve here) 
```
* for magnitude find 2s compliment of inverted bit
```
~x = 28 leading 1111 and 1001 and msb shows the sign (-ve here) 
for 2s compliment invert all the bit and add 1
x = 1111 1001 
after invert the bit
x = 0000 0110 
          + 1
-------------------------
    0000 0111       =  7
```
* magnitude is 7 and signm is negative so -7 result
```cpp
#include <iostream>
using namespace std;

int main() {
  int b = 6;
  int c = (~b);
  cout << c << endl; // -7
}
```
## Binary left shift(<<)

```
5 << 2
5 = 0000 0101 left shift 2 bit 0001 0100 result will be 20
```
* x << y is equivalent to x * 2^y

```cpp
#include <iostream>
using namespace std;

int main() {

  cout << (5 << 2) << endl; // 20
  
}
```
## Binary right shift(<<)

```
5 >> 2
5 = 0000 0101 right shift 2 bit 0000 0001 result will be 1
```
* x >> y is equivalent to x / 2^y

```cpp
#include <iostream>
using namespace std;

int main() {

  cout << (5 >> 2) << endl; // 1
  
}
```
