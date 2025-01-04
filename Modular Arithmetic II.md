Picking up from Modular Arithmetic I, imagine we've picked up a modulus p, and now we will restrict ourselves to the case when p is prime.

The integers modulo p define a field, denoted F<sub>p</sub> . 

A finite field ​F<sub>p</sub> is the set of integers 0,1,...,p−1 and under both addition and multiplication there are inverse elements b<sub>+</sub>​ and b<sub>*</sub>​ for every element `a` in the set, such that a+ b<sub>+</sub>=0 and a⋅ b<sub>*</sub>=1 . 

Let's say you pickup **p=17**.  Calculate 3<sup>17</sup> mod 17. Now do the same with 5<sup>17</sup> mod 17

same for 7<sup>16</sup> mod 17 

**We have to look at Fermat's little theorem.**  *(We need this when we look at RSA cryptography)*

#### Fermat's little theorem

It states that **if p is a prime number**, then for any integer a, the number a<sup>p</sup> - a is an integer multiple of p.

a<sup>p</sup> ≡ a (mod p)

**If p is not divisible by a i.e. coprime,** then the theorem is equivalent to a<sup>p-1</sup> -1 is an integer multiple of p.

a<sup>p-1</sup> ≡ 1 (mod p)

**Question: **

![[Pasted image 20241026000606.png]]
*Notice how it ressembles with the second case of Fermat's Little Theorem hehe *
