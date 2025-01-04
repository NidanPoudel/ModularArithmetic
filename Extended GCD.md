Let a and b be positive integers.

The **extended Eucledian Algorithm** is and efficient way to find the integers u,v such that

`a.u + b.v = gcd(a,b)`

*When decrypting RSA ciphertexts, this algorithm is used to calculate the modular inverse of the public exponent.*

In the standard Eucledian algorithm , the quotients are not used. Only the remainders are kept. But for the extended algorithm, the successive quotients are also used. 

 The standard Euclidean algorithm with _a_ and _b_ as input, consists of computing a sequence q1,…,qk of quotients and a sequence r0,…,rk+1 of remainders such that

```
r0 = a 
r1 = b
r(i+1) = r(i-1)-q(i)r(i) 
```

The computation stops when one reaches a remainder r(k+1) which is zero; the greatest common divisor is then the last non zero remainder r(k).

#### Code :

```python
def extended_gcd(a,b):

    old_r, r = a, b

    old_s, s = 1, 0

    old_t, t = 0, 1

    while(r!=0):

        q = old_r // r

        old_r, r = r, old_r - q * r

        old_s, s = s, old_s - q * s

        old_t, t = t, old_t - q * t

        print("-")

    print(f'gcd: {old_r}, {old_s},{old_t}')

  

extended_gcd(26513,32321)
```
