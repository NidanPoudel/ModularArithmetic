We've looked at multiplication and division in modular arithmetic, but what does it mean to take the square root modulo an integer?

For the following discussion, let's work modulo p=29. We can take the integer a=11 and calculate  a<sup>2</sup> = 5 MOD 29

As a = 11, a<sup>2</sup> =5, we say that square root of 5 is 11.

*Now let's think about square root of 18.*
Firstly, we have to find an integer `a` such that a<sup>2</sup> = 18.

![[Pasted image 20241026064842.png]]

#### Main Statement
We say that an integer x is a _Quadratic Residue_ if there exists an a such that 
a<sup>2</sup> ≡ x mod p. If there is no such solution, then the integer is a _Quadratic Non-Residue_.

So in other words, x is an quadratic residue if it's possible to take square root of x modulo an integer p.

##### Question 

In the below list there are two non-quadratic residues and one quadratic residue.  
  
Find the quadratic residue and then calculate its square root. Of the two possible roots, submit the smaller one as the flag. 

**two possible roots because** If a<sup>2</sup>=x then (−a)<sup>2</sup>=x. So if x is a quadratic residue in some finite field, then there are always two solutions for a.

`p = 29, ints = [14,6,11]`

#### Solution

```python
p=29

ints =[14,6,11]

temp = 0

for i in range(1,p-1):

    temp = (i*i) % p

    if temp in ints:

        print(temp)

        break

  

for i in range(1,p-1):

    if((i*8)%p==temp):

        print(i)
```