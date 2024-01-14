# Quantum-Computing
Quantum computing using the IBM Virtual Quantum Lab

SHOR’S ALGORITHM

DEFINITION
Shor’s algorithm is famous for factoring integers in polynomial time. Since the best-known
classical algorithm requires greater-than-polynomial time to factor the product of two primes, the
widely used cryptographic protocol, RSA, relies on factoring being impossible for large enough
integers.
We will focus on the quantum part of Shor’s algorithm, which actually solves the problem of
period finding. Since a factoring problem can be turned into a period finding problem in
polynomial time, an efficient period finding algorithm can be used to factor integers efficiently
too. For now its enough to show that if we can compute the period of efficiently,
then we can also efficiently factor. Since period finding is a worthy problem in its own right, we
will first solve this, then discuss how this can be used to factorize numbers.

PERIOD FINDING
Let’s look at the periodic function: ![image](https://github.com/kart2004/Quantum-Computing/assets/111494403/ad924cac-a976-4029-b2d5-e0d2ccba858e)

where a and N are positive integers, a is less than N, and they have no common factors. The
period, or order r, is the smallest (non-zero) integer such that: ![image](https://github.com/kart2004/Quantum-Computing/assets/111494403/6435cb10-77f0-459f-b8d1-b51b9b25f4c8)

We can see an example of this function plotted on the graph below. Note that the lines between
points are to help see the periodicity and do not represent the intermediate values between the
x-markers.
