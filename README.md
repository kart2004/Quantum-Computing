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

SHOR’S SOLUTION
QISKIT IMPLEMENTATION
In this example we will solve the period finding problem and we provide the circuits for : ![image](https://github.com/kart2004/Quantum-Computing/assets/111494403/04da4767-f788-4b39-af7a-067559bd62e0)


To create Ux, we will simply repeat the circuit times, resulting in controlled multiplication.
The code on the right is used for inverse quantum phase transformation.

Let us take n = 15 as a test case, we check if they are co-prime by using the gcd operator.

This code effectively implements Quantum Phase Estimation to estimate the phase of the unitary
operator corresponding to the modular multiplication a^r mod 15

Then we use the qpe_amod15(a) function to estimate a phase and then converting that phase into
a simplified fraction using Python's Fraction class. Finally, we are extracting the numerator and
denominator of the simplified fraction.

The next step is trying to find possible factors of N using the values a, r, and the estimated values
of s and r

The code then runs the loop and checks if the guessed factors are non-trivial and factors of N. If
it finds a non-trivial factor, it sets FACTOR_FOUND to True, breaks out of the loop, and prints
the factor.

This code effectively implements Shor's algorithm to factor N using a specific value of a. It may
require multiple attempts to find a factor, and it will eventually terminate when a factor is found
or when the loop reaches a certain number of attempts.

IBM GATES REPRESENTATION:

CONCLUSION:
In conclusion, quantum gates are pivotal in the development of quantum computing, enabling the
manipulation of qubits in ways that classical gates cannot replicate. As we look to the future,
there is considerable work ahead. Researchers are focused on expanding the toolbox of quantum
gates, optimizing their performance, and developing fault-tolerant quantum error correction
techniques. Additionally, the integration of quantum gates into practical applications, from
cryptography to optimization problems, holds immense promise. The continued exploration of
quantum gates and their applications will undoubtedly lead to groundbreaking advancements in
both quantum technology and our understanding of the quantum world.


