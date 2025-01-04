As we've seen, we can work within a finite field F<sub>p</sub>​, adding and multiplying elements, and always obtain another element of the field.

For all elements g in the field, there exists another number d such that `g.d ≡ 1 mod p`

This is the multiplicative inverse of `g`

Example : `7.8 = 56 ≡ 1 mod 11 `

##### Question
What is the inverse element d= 3<sup>-1</sup> such that 3.d ≡ 1 mod 13

Solution: 
```python 
p=13
for num in range (1,p-1):

    if((num*3)%13 ==1):

        print(num)

        break
```
