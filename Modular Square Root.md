In Legendre Symbol we introduced a fast way to determine whether a number is a square root modulo a prime. We can go further: there are algorithms for efficiently calculating such roots.
The best one in practice is called Tonelli-Shanks, which gets its funny name from the fact that it was first described by an Italian in the 19th century and rediscovered independently by Daniel Shanks in the 1970s.

![[Pasted image 20241026082655.png]]

![[Pasted image 20241026083358.png]]

**The main use case for this algorithm is to find the elliptic curves coordinates.** 
*Its operation is somewhat complex so we're not going to discuss the details, however, implementations are easy to find and Sage has one built-in.*

#### Question

Find the square root of a modulo the 2048-bit prime p. Give the smaller of the two roots as your answer.

### Solution
Save this in a .sage extension file and run

```python
# Define the values of a and p
a = 8479994658316772151941616510097127087554541274812435112009425778595495359700244470400642403747058566807127814165396
p = 3053185186199433325267593511148795069441433276390908351413376986135096089507650468726136981573574254942878913830084

# Create a finite field GF(p)
F = GF(p)

# Find the square root of a in the field
sqrt_a = F(a).sqrt()

# Print the smaller of the two roots
print(min(sqrt_a, -sqrt_a))
```
