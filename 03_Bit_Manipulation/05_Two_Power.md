## Check Number is power of two or not
```
16 = 2^4
8  = 2^3
```
```
n = 16    => 0000 0001 0000
n-1 = 15  => 0000 0000 0111
n & (n-1) => 0000 0000 0000 = 0 i.e power of two
```
```cpp
#include <iostream>
using namespace std;

int main() {
  int n;
  cin >> n;

  if((n & (n-1)) == 0) {
    cout << "power of two" << endl;
  }
  else {
    cout << "not power of two" << endl;
  }
  return 0;
}
```
