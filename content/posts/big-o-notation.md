---
title: "Big-O Notation"
tags: ['BigO']
categories: ['data structure','algorithm']
date: 2022-02-10T13:40:30+07:00
author: 'me'
---
## Defination

>**f(n) = O(g(n))** or **f(n) ≤ g(n)**  
>if there exist constants **N** and **c**,  
>**n ≥ N , f(n) ≥ c*g(n)**  

## Common Rule
>**Multiplcative constants can be omitted**  
>
>`**n^3** = O(**n^3**)  
**n^2**/3 = O(**n^2**)`  
>
>**n^a < n^b for 0 < a <b :**  
>`n = O(n^2), root(n) = O(n)`  
>***using *__n for a__* and __n for b__*  
>
>**n^a < b^n (a>0,b>1) :**  
>`n^5 = O(root(2^n), n^100 = O(1.1^n)`  
>
>**(log n)^a < n^b (a,b > 0) :**  
>`(log n)^3 = O(root(n)), n log n = O(n^2)`  
>
>**Smaller terms can be omitted**  
>`
n^2 + n(smaller than n^2) = O(n^2), *2^n + n^9(smaller than 2^n) = O(2^n)`  
>
Big O will combine together like  
```
O(1)+O(1)+O(n)*O(n)+O(1) = O(n)*O(n)
O(n)*O(n) = O(n^2)
```
## Other Notation
>### Defination
>- For functions f,g : N -> R+ we say that:  
>
>   - f(n) = Ω(g(n)) or f >= g if for some c,  
>  f(n) >= c*g(n) (f grows no slower than g).  
>
>   - f(n) = Θ(g(n)) or f ≈ g if f = O(g)  
> and f =  Ω(g) (f grows at the same rate as g).  
>
>   - f(n) = o(g(n)) or f < g if f(n)/g(n) ==0 as n = ∞  
> (f grows slower than g)
>

![img](https://miro.medium.com/max/1200/1*5ZLci3SuR0zM_QlZOADv8Q.jpeg)


```
    3n² + 5n + 2 = O(n²) since if n ≥ 1
    3n² + 5n + 2 ≤ 3n² + 5n² + 2n² = 10n²
```
![img](/blog/function/big-o-growth-rate.PNG)