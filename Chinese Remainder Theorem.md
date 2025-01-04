The Chinese Remainder Theorem gives unique solution to the et of linear congruences if their moduli are coprime.

![[Pasted image 20241026091647.png]]

**In cryptography, we commonly use the Chinese Remainder Theorem to help us reduce a problem of very large integers into a set of several, easier problems.**

![[Pasted image 20241026094429.png]]
#### Question

![[Pasted image 20241026091838.png]]

From the Gauss algoithm presented in picture (white background) above, we write a solution using python: 
```python
from sympy import mod_inverse

a_values = [2,3,5]

mod_values = [5,11,17]

  

def chinese_remainder_theorem(remainders,moduli):

    N=1

    for num in moduli:

        N*=num

    x =0

    for remainder,modulus in zip(remainders,moduli):

        Ni=N//modulus

        Mi=mod_inverse(Ni,modulus)

        x += remainder*Ni*Mi

    return x%N

  

print(chinese_remainder_theorem(a_values,mod_values))
```
