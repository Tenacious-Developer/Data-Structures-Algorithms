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
f(n) <= g()
* Big-omega(Ω) -> minimum (lower bound) -> best case
* Big-theta(Θ) -> upper bound = lower bound 
