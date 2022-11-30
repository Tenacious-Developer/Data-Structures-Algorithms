# Asymptotic Notations:
* Mathematical way of representing the complexity of a algorithm
* Represent both time & space complexity
### Big-oh(O)
* Big-oh(O) -> maximum (upper bound) -> worst case
* An upper bound of time and space taken by an algorithm
* Upper bound means maximum time or space taken by an algorithm while execution
* L.H.S <= R.H.S
```
f(n) = O(g(n))
if
f(n) <= c*g(n)

so f(n) function will take maximum O(n) time
```
* f(n) = (+ve) function to represent complexity of any algorithm(e.g f(n) = n^2 + n +10)
* g(n) = (+ve) function which belongs to complexity function(e.g O(1), O(n^2))
* c is some real positive constant, c > 0
* n0 is (+ve) initial input size (e.g. if input (n) range is from 1 to 100, then n0 = 1), n >= n0, n0 > 0
```
f(n) = O(g(n))

f(n) = n + 10
g(n) = n

sollution:
f(n) <= c*g(n)
n+10 <= c*n
for satisying this 
c = 2
n0 = 10

So above function satisfy fron n0 = 10 to infinity
```
```
n   = O(n^2)--------T
n   = O(n)----------T
n^2 = O(n^3)--------T
n^2 = O(n^2 - 10)---T
```
### Big-omega(Ω)
* Big-omega(Ω) -> minimum (lower bound) -> best case
* An lower bound of time and space taken by an algorithm
* Lower bound means minimum time or space taken by an algorithm while execution
* L.H.S >= R.H.S
```
f(n) = Ω(g(n))
if
f(n) > = c*g(n)

so f(n) function will take minimum Ω(n) time
```
* f(n) = (+ve) function to represent complexity of any algorithm(e.g f(n) = n^2 + n +10)
* g(n) = (+ve) function which belongs to complexity function(e.g Ω(1), Ω(n^2))
* c is some real positive constant, c > 0
* n0 is (+ve) initial input size (e.g. if input (n) range is from 1 to 100, then n0 = 1), n >= n0, n0 > 0
```
f(n) = Ω(g(n))

f(n) = n
g(n) = n + 10

sollution:
f(n) >= c*g(n)
n >= c*(n+10)
for satisying this 
c = 1/6
n0 = 2

So above function satisfy fron n0 = 2 to infinity
```
```
n   = Ω(n^2)--------F
n   = Ω(n)----------T
n^3 = Ω(n^2)--------T
n^2 = Ω(n^2 - 10)---T
```
### Big-theta(Θ)
* Big-theta(Θ) -> upper bound = lower bound 
* A lower bound & upper bound of time and space taken by an algorithm is same
* L.H.S = R.H.S
```
f(n) = Θ(g(n))
if
f(n) <= c1*g(n) && f(n) >= c2*g(n)

so f(n) function will take equal Θ(n) time
```
* f(n) = (+ve) function to represent complexity of any algorithm(e.g f(n) = n^2 + n +10)
* g(n) = (+ve) function which belongs to complexity function(e.g Θ(1), Θ(n^2))
* c1 & c2 is some real positive constant,which need not be having same value of c1 & c2, and c1,c2 > 0
* n0 is (+ve) initial input size (e.g. if input (n) range is from 1 to 100, then n0 = 1), n >= n0, n0 > 0
```
f(n) = Θ(g(n))

f(n) = n
g(n) = n + 10

sollution:
f(n) >= c1*g(n)
f(n) <= c2*g(n)

n >= c1*(n+10)
n <= c2*(n+10)
for satisying this 
c1 = 1
c2 = 1/11
n0 = 1

So above function satisfy fron n0 = 1 to infinity
```
```
n   = Θ(n^2)--------F
n   = Θ(n)----------T
n^3 = Θ(n^2)--------F
n^2 = Θ(n^2 - 10)---T
```
* Θ notation does not represent average case complexity
### Types of Upper Bound
* Upper bound ---> (big-oh) ---> L.H.S <= R.H.S
  * Tightly upper bound
    * L.H.S = R.H.S  (3n = o(n))
  * Lossely upper bound
    * L.H.S < R.H.S  (3n < o(n^2))
```
n    = o(n^2)---LUB
n    = o(n)-----TUB
n^2  = o(n^3)---LUB
n+10 = o(n)-----TUB
```
### Little-oh(o)
* Little-oh(o) ->(loosely upper bound) 
* A loosely upper bound of time and space taken by an algorithm 
* L.H.S < R.H.S
```
A = o(B)
iff
A < B
```
```
n   = o(n^2)--------T
n   = o(n)----------F
n^2 = o(n^3)--------T
n^2 = o(n^2 - 10)---F
```
### Types of Lower Bound
* Lower bound ---> (big-omega) ---> L.H.S >= R.H.S
  * Tightly lower bound
    * L.H.S = R.H.S  (3n = Ω(n))
  * Lossely lower bound
    * L.H.S > R.H.S  (3n < Ω(n^2))
```
n^3   = Ω(n^2)---LLB
n    = Ω(n)-----TLB
n+10 = Ω(n)-----TLB
```
### Little-omega(w)
* Little-omega(w) ->(loosely lower bound) 
* A loosely lower bound of time and space taken by an algorithm 
* L.H.S > R.H.S
```
A = w(B)
iff
A > B
```
```
n^2   = w(n)--------T
n     = w(n)----------F
n^3   = w(n^2)--------T
n^2   = w(n^2 - 10)---F
```
