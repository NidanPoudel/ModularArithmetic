
### The Steps of Euclid's Algorithm:

1. **Start with two positive integers** a and b (where a≥ba \geq ba≥b).
2. **Compute the remainder** r of the division of a by b: r=amod  br = a \mod br=a mod b
3. **Replace** a with b and b with r.
4. **Repeat** steps 2 and 3 until bbb becomes 0. The GCD is the last non-zero remainder.

```python
a= 66528

r=52920

b=0

while(r!=0):

    b=r

    r= a%b

    a=b

print(b)
```
