# QOSF_Tasks

## Problem Statement

```
Task 1 find the largest number

You have two integers, either positive or negative, and the challenge is to generate a quantum algorithm that returns which is the larger number. Consider an appropriate number of qubits and explain why your proposal is valid for all kinds of numbers in case 


def find_the_largest_number (int:number_1, int ,number_2):
     “””
 number_1 : integer value that is the first parameter to the function,
number_2 : integer value that is the second parameter to the function.
Return the largest number between number_1 and number_2
     “””

     # use a framework that works with quantum circuits, qiskit, cirq, pennylane, etc. 

      # consider print your quantum circuit,


Example:

A = find_the_largest_number(5,-6)
print(A)

“5”

References:

[1] Deutsch, David, and Richard Jozsa. "Rapid solution of problems by quantum computation." Proceedings of the Royal Society of London. Series A: Mathematical and Physical Sciences 439.1907 (1992): 553-558.
[2] Bernstein, Ethan, and Umesh Vazirani. "Quantum complexity theory." SIAM Journal on computing 26.5 (1997): 1411-1473.
[3] Grover, Lov K. , "A fast quantum mechanical algorithm for database search", Proceedings of the 28th Annual ACM Symposium on the Theory of Computing (1996), arXiv:quant-ph/9605043

```

Here I implemented the quantum comparison algorithm which relies on controlled rotation shift of the target qubit, this phase kickback is dependent on the comparison between the two integers.
If `a>b` (constructive interference) the phase kickback is positive and if `a<b`phase kickback is negative (destructive interference).

I applied the inverse fourier transform to measure the final result of qubits.

```
q0, q1 :: input qubits
q3, q4 :: auxilary qubits
q5 :: comparison result
q6 :: output

```

The above solution will work for any 2 n-bit numbers since no assumption is made about the length of the bits in the given numbers. 

Other References Used:
* arXiv:quant-ph/0411037
 (or arXiv:quant-ph/0411037v1 for this version)
 https://doi.org/10.48550/arXiv.quant-ph/0411037

* https://quantumalgorithmzoo.org/
