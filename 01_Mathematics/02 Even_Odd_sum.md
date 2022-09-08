## Problem:
* Find out the even digit number sum & odd digit number sum
* Input : 23456
* Output : even sum = 2+4+6 => 12 & odd sum = 3+5 => 8

### Logic:
* run a loop till number > 0.
* find out last digit through modulus & check that number is even or odd
* add the even number in even variable & odd number in odd variable

### Code:
```cpp
#include <iostream>
using namespace std;
int evenSum(int x) {
	int sum = 0;
	int digit;
	while(x>0) {
		digit = x % 10;
		if (digit % 2 == 0 ){
			sum += digit;
		}
		x = x/10;
	}
	return sum;
}

int oddSum(int x) {
	int sum = 0;
	int digit;
	while(x>0) {
		digit = x % 10;
		if (digit % 2 != 0 ){
			sum += digit;
		}
		x = x/10;
	}
	return sum;
}
int main() {
	int num;
	cin >> num;

	int even_sum = evenSum(num);
	cout << even_sum << endl;
	int odd_sum = oddSum(num);
	cout << odd_sum << endl;
	
	
}
```     
