# Complexity Analysis:
### Algorithm:
* Finite steps to solve a problem in finite amount of time.
### Time Complexity:
* Amount of time taken by the algorithm to run as function of the input size.
* Constant = O(1) - no loop
* Logrithmic = O(log n) - usually searching algorithm have log n if they are sorted(binary search)
```
for(i = 1; i <= n; i = 2*i) --- log n
if n = 16 then we have traverse 4 time to rach 16 i.e log 16 = 4
```
```
for(i = n; i <= 1; i = i/2) --- log n
similarly in rever order
```
```
for(i = n; i <= 1; i = i/2) ------ log n
  for(j = 1; j <= n; j = j*2) ----------- log n
  
so time complexity = log n * log n = (log n)^2
```
* Linear = O(n) - for loop, while loop through n times
```
for(i = 1; i <= n; i++)
```
* Log Linear = (n logn) - usually sorting algorithm
```
for(i = 1; i <= n; i++) -------- n
  for(j = 1; j <= n; j = j*2) ------- log n
  
so time complexity = n * log n = (n log n)
```
* log(log n)
```
for(i = 2; i <= n; i = i^2) -------- log(log n)
if n = 16 then we have traverse 4 time & log of 4 is 2 so 2 traverse to rach 16 i.e log(log 16) = log(4) = 2
```
* Quadratic = O(n^2) - two nested loops
```
for(i = 1; i <= n; i++) -------- n
  for(j = 1; j <= n; j++) ------- n
  
so time complexity = n * n = (n^2)
```
* Exponential = O(2^n) - recursive algorithm that solve a problem of size n
* Factorial = O(n!) - adding a loop for every element 
* O(m*n)
```
for(i = 1; i <= m; i++) -------- n
  for(j = 1; j <= n; j++) ------- n
  
so time complexity = m * n = (m*n)
```
* O(m+n)
```
for(i = 1; i <= m; i++) -------- m
for(j = 1; j <= n; j++) ------- n
  
so time complexity = m * n = (m+n)
```
### Time Complexity Increases
```
O(1)
O(log n)
O(n)
O(n^2)
O(2^n)
O(n!)
```
### What can cause time in a Function
* Operations(+, -, *, /)
* Comparison(<, >, ==)
* Looping(for, while)
* Outside function call
### What can cause space complexity 
* Variables
* Data Structures
* Function Call
* Allocations

### Note
* DRY
* avoid nested loop except of this, use two seprate loops(less time complexity)
* Low space complexity ---> Recursion can cause stack overflow and copying of large arrays may exceed memory
* Hash maps are used to improve time complexity
* for sorted arrays use binary tree to achive O(log n)
* Hash tables and precomputed information (i.e Sorted) are some of the best ways tooptimise code 
