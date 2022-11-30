# Comparing growth of complex complexity functions
* Informal method to predict which function grow faster w.r.t other function
* 1) Remove the common term both side
* 2) Apply log function both side
* 3) After applying both rule 1 & 2 not able to decide then put some large input value on both side
* All these steps applying in sequence only
```
Question: n vs n^2
sollution: remove the common term
n vs n^2
1 vs n
1 < n

n grows fater then 1
n = o(n^2) LUB
```
```
Question: nlogn vs n^2
sollution:remove the common term
nlogn vs n^2
logn vs n
1ogn < n

n grows fater then logn
n = o(n^2) LUB
```
```
Question: 2^n vs n^n
sollution: apply log function on both side 
log2^n vs logn^n
nlog2 vs nlogn
n vs nlogn
n < nlogn

nlogn grows fater then n
n = o(n(logn)) LUB
```
```
Question: log2^(2^n) vs log2^n
sollution:
remove common terms
log2^(2^n) vs log2^n
2^nlog2 vs nlog2
2^n vs n
apply log on both side
log2^n vs logn
nlog2 vs logn
n*1 vs logn
n vs logn
n > logn

n grows fater then logn
n = w(log2^n) LUB
```
