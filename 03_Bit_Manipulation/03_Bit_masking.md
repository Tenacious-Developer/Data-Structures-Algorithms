## Get i th Bit

* n = 5 => 0000 0101 and find 3 bit i.e 0
* mask = 1 << i (i = 3)
* perform & operation (n & mask)
    * non-zeros then result will be 1
    * zeros then result will be 0

### Pseudocode
```
int getIthBit(int n,int i){
	int mask = (1 << i);
	return (n & mask) > 0 ? 1 : 0;
}
```
### CPP
```cpp
#include <iostream>
using namespace std;

int getIthBit(int n,int i){
	int mask = (1 << i);
	return (n & mask) > 0 ? 1 : 0;
}
int main() {
    int n = 5;
    int i;
    cin >> i;

    cout << getIthBit(n, i) << endl; 

    return 0;
}
```
## Set i th Bit

* n = 5 => 0000 0101 and set 3 bit to 1
* mask = 1 << i (i = 3)
* perform | operation (n | mask)
```
5        = 0101
mask     = 1000
5 | mask = 1101 = 13
```

### Pseudocode
```
void setIthBit(int n,int i){
    int mask = (1 << i);
    n = (n | mask);
    cout << n << endl;
  }
```
### CPP
```cpp
#include <iostream>
using namespace std;

void setIthBit(int n,int i){
  int mask = (1 << i);
  n = (n | mask);
  cout << n << endl;
}

int main() {
    int n = 5;
    int i;
    cin >> i;

    setIthBit(n,i);

    return 0;
  }
```
## Clear i th Bit
* n = 5 => 0000 0101 and clear 2 bit 
```
5 = 0101 after clear 0001 i.e 1
```
* mask = ~(1 << i) i = 2
* perform & operation (n & mask)
```
5            = 0101
(1 << 2)     = 0100
~(1 << 2)    = 1011 
now 5 & (~(1 << 2)) = 0101
                      1011
                  ----------
                      0001 = 1
```

### Pseudocode
```
void clearIthBit(int n,int i){
    int mask = ~(1 << i);
    int res = (n & mask);
    cout << res << endl;
  }
```
### CPP
```cpp
#include <iostream>
using namespace std;

void clearIthBit(int n,int i){
  int mask = ~(1 << i);
  int res = (n & mask);
  cout << res << endl;
}

int main() {
    int n = 5;
    int i;
    cin >> i;

    clearIthBit(n,i);

    return 0;
  }
```
## Update i th Bit
* n = 5 => 0000 0101 and update 1 bit by value of 1
```
5 = 0101 after update 0111 i.e 7
```
* mask = (v << i) i = 1
* perform or operation (n | mask)
```
5            = 0101
(1 << 1)     = 0010 
now 5 & (1 << 2) = 0101
                   0010
                  ----------
                   0111 = 7
```

### Pseudocode
```
void updateIthBit(int n,int i,int v){
	clearIthBit(n,i);
	int mask = (v << i);
	int res = (n | mask);
	cout << res << endl;
}
```
### CPP
```cpp
#include <iostream>
using namespace std;

void clearIthBit(int n,int i){
  int mask = ~(1 << i);
  int res = (n & mask);
  cout << res << endl;
}

int main() {
    int n = 5;
    int i;
    cin >> i;

    updateIthBit(n,i,1);

    return 0;
  }
```
## Clear last i th Bit
* n = 15 => 0000 1111 and clear last 2 bit
```
5 = 1111 after clear last 2 bit 1100 i.e 12
```
* integer value 0 in bitwise form = 0000 0000 ....
* ~(0) = 1111 1111 .... = (-1)
* mask = (-1 << i) 
* perform & operation (n & mask)
```
15                 = 1111
(-1 << 2)          = 1100

now 15 & (-1 << 2) = 1111
                     1100
                  ----------
                     1100 = 12
```

### Pseudocode
```
void clearLastIthBit(int n, int i){
	int mask = (-1 << i);
	int res = (n & mask);
	cout << res << endl;
}
```
### CPP
```cpp
#include <iostream>
using namespace std;

void clearLastIthBit(int n, int i){
	int mask = (-1 << i);
	int res = (n & mask);
	cout << res << endl;
}

int main() {
    int n = 5;
    int i;
    cin >> i;

    clearLastIthBit(n,i);

    return 0;
  }
```
