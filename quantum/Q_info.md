----
> ### Qiskit
----

----
> ### Installation
----
```
sudo apt install python3-pip
pip3 install qiskit
sudo apt  install jupyter-core
sudo apt install jupyter-notebook
jupyter-notebook           
jupyter notebook
pip install matplotlib
pip install pylatexenc
pip install git+https://github.com/qiskit-community/qiskit-textbook.git#subdirectory=qiskit-textbook-src
pip install numexpr

```
----
> ### 4_Representations
----
bit similarly quibit

> BRACKET 

* x | 0 > = | 1 
x gate applied to state 0 gives state 1

> MATRIX
* * xgate&nbsp;&nbsp;&nbsp;0&nbsp;&nbsp;&nbsp;&nbsp;=&nbsp;&nbsp;&nbsp;1

* * [0&nbsp;1]&nbsp;&nbsp;&nbsp;[ 1 ]&nbsp;&nbsp;&nbsp;=&nbsp;&nbsp;&nbsp;[ 0 ]

* * 1&nbsp;&nbsp;0&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;0&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1

* `circuit.x(0)`    # not cx ... its different..... 0 is refering to q1 bit 
* * o/p > [0 ]   is 1 (One)
* * &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1


* [0.+0.j     1.+0.j]  is 1 (One)


* matrix multi : In general, matrix mutiplication between two matrices involves taking the first row of the first matrix, and multiplying each element by its "partner" in the first column of the second matrix (the first number of the row is multiplied by the first number of the column, second number of the row and second number of column, etc.). The sum of these new numbers becomes the first element of the first row of the new matrix. To fill in the rest of the first row, we repeat this process for the second, third, etc. columns of the second matrix. Then we take the second row of the first matrix, and repeat the process for each column of the second matrix, to produce the second row. We perform this process until we have used all rows of the first matrix. The resulting matrix is our new matrix.
* ![Screenshot from 2022-03-20 12-05-33](https://user-images.githubusercontent.com/25542518/159151187-1c96a524-96ca-49e6-bcdd-a6cad5049d7d.png)

> BLOCH SPHERE
* radius of the Bloch sphere is 1

> MEASUREMENT

----
> ### Doc Liner Algebra
----
> Vectors and spaces 
* | V >  is defined as elements of a set known as a vector space. A more intuitive and geometric definition is that a vector "is a mathematical quantity with both direction and magnitude"
* x  and y components of the form (3)  : 3 units along the x axis and 5 units along the y axis.
                                   5


> Matrix
* We manipulate qubits in our quantum computer by applying sequences of quantum gates. Each quantum gate can be expressed as a matrix that can be applied to state vectors, thus changing the state.
* Pauli-X gate > xgate > σ symbol
* * ![Screenshot from 2022-03-26 15-19-54](https://user-images.githubusercontent.com/25542518/160234201-8f430750-cca5-4f4e-b9d0-f197cdb19f92.png)
* Pauli x y z
* * ![download (3)](https://user-images.githubusercontent.com/25542518/160234566-3df707ad-9fde-4ae5-b101-2b1ed3c8bc76.png)
* Hermitian and Unitary matrices
* * A Hermitian matrix is simply a matrix that is equal to its conjugate transpose (denoted with a † symbol)  -- conjugate changing signs
* * Paulis matrix is hermatian
* * ![Screenshot from 2022-03-20 12-27-39](https://user-images.githubusercontent.com/25542518/159151837-34a15952-6c55-4b59-ae0c-92f222749fd1.png)
* A unitary matrix is very similar. Specifically, it is a matrix such that the inverse matrix is equal to the conjugate transpose of the original matrix.
* The inverse of some matrix  A , denoted as  A−1 , is a matrix such that where I is the identity matrix.
* * ![Screenshot from 2022-03-26 11-36-57](https://user-images.githubusercontent.com/25542518/160227148-5f378824-3853-4772-a664-8a57f20a763d.png)
* The Pauli-Y matrix, in addition to being Hermitian, is also unitary
* * ![Screenshot from 2022-03-26 11-45-54](https://user-images.githubusercontent.com/25542518/160227352-766f478f-a1ae-4234-bbd2-7b87420a52a6.png)
* **The basic idea is that evolution of a quantum state by application of a unitary matrix "preserves" the norm (magnitude) of the quantum state.**

> Spanning Sets, Linear Dependence, and Bases 
> Hilbert Spaces, Orthonormality, and the Inner Product
* A Hilbert space can be thought of as the state space in which all quantum state vectors "live". The main difference between a Hilbert space and any random vector space is that a Hilbert space is equipped with an inner product, which is an operation that can be performed between two vectors, returning a scalar.
* For two vectors  |a⟩  and  |b⟩  in a Hilbert space, we denote the inner product as  ⟨a|b⟩ , where  ⟨a|  is equal to the conjugate transpose of  |a⟩ , denoted  |a⟩† . Thus, the inner product between two vectors of the Hilbert space looks something like:
* * ![Screenshot from 2022-03-26 12-57-14](https://user-images.githubusercontent.com/25542518/160229505-b7649f71-f335-4d75-b4c7-bba9ba75fb92.png)
* * One of the most important conditions for a Hilbert space representing a quantum system is that the inner product of a vector with itself is equal to one: ⟨ψ|ψ⟩ = 1. This is the so-called normalization condition, which states that the length of the vector squared (each component of the vector is squared and summed together, by definition of the inner product) must be equal to one.
* This means that unitary evolution sends quantum states to other valid quantum states. For a single-qubit Hilbert space, represented by the Bloch sphere, unitary transformations correspond to rotations of state vectors to different points on the sphere, not changing the length of the state vector in any way.
> Outer Products 
* Inner products aren't the only way to multiply vectors. Occasionally, we'll switch the order of the bra and ket in order to take the outer product, whose outcome is a matrix, rather than a single number. For two vectors  |a⟩  and  |b⟩  in a Hilbert space, we denote the outer product as  |a⟩  ⟨b| , where  ⟨b|  is equal to the conjugate transpose of  |b⟩
* ![Screenshot from 2022-03-26 14-40-21](https://user-images.githubusercontent.com/25542518/160232814-945890e1-86d7-4aac-8495-a9fd5f8d1ef8.png)
> tensor product 
* Most often, you'll see the tensor product used to describe the shared state of two or more qubits. Notice here that the tensor product doesn't require taking one of the vector's conjugate transposes like the outer product does—we're multiplying two kets together instead of a ket and a bra. The tensor product of vectors  |a⟩  and  |b⟩ , written  |a⟩⊗|b⟩  or  |ab⟩ , equals:
* ![Screenshot from 2022-03-26 14-45-25](https://user-images.githubusercontent.com/25542518/160233000-151b9fa9-7cfd-4168-ae49-aed47c27c722.png)

> Eigenvectors and Eigenvalues 
* ![Screenshot from 2022-03-26 15-46-04](https://user-images.githubusercontent.com/25542518/160235041-0cfb3a48-b954-40ba-8031-67afcfcf51ef.png)
* where  A  is a matrix, and  λ  is some number. If we are given some matrix  A , and need to find the vectors  |v⟩  and numbers  λ  that satisfy this relationship, we call these vectors eigenvectors, and their corresponding number multipliers eigenvalues. 
* _**In fact, the following properties are very important in gate model of quantum computation, where we deal with finite dimensional vector spaces:
A Hermitian matrix has linearly independent eigenvectors. The number of these eigenvectors is equal to the dimension of the vector space. In addition, when the corresponding eigenvalues are distinct, the eigenvectors are orthogonal. When the eigenvalues are the same, the eigenvectors are not orthogonal, but they are still linearly independent and can be orthogonalized. Therefore, eigenvectors of a Hermitian matrix form a basis for the vector space.
Since a unitary matrix is a normal matrix, the eigenvectors of a unitary matrix form an orthonormal basis for the vector space.
As an important special case, these can be verified for each of the Pauli matrices.**_
> Matrix Exponentials 
* Taylor series, involutory matrix, Maclaurin series
----
> ### Doc Atoms and computation
----
> Binary to Decimal - 2 ways
![Screenshot from 2022-03-27 09-21-03](https://user-images.githubusercontent.com/25542518/160269054-b8196c6a-a929-4230-9661-b8ce438ba81e.png)
![Screenshot from 2022-03-27 09-21-20](https://user-images.githubusercontent.com/25542518/160268986-a6a0bfa4-0a01-4a63-9d25-ad8c103ae870.png)
![Screenshot from 2022-03-27 12-28-07](https://user-images.githubusercontent.com/25542518/160270427-03fbc680-4628-4583-8965-d345e05fd33f.png)


> Computation Diagram
![Screenshot from 2022-03-27 09-35-43](https://user-images.githubusercontent.com/25542518/160268971-1e9476de-9a6f-4285-8692-c41ef1181fbf.png)



> Creating an Adder Circuit 
> > Encoding Input
* It simply flips the bit value: 0 becomes 1 and 1 becomes 0. For qubits, it is an operation called x that does the job of the NOT.
* Qubits are always initialized to give the output 0.
* * Qiskit numbers the bits in a string from right to left.
* * 10000000
* * Specifically, it means that qubit 7 is telling us about how many 2^7s we have in our number. So by flipping this bit, we’ve now written the number 128 in our simple 8-bit computer.

* * eg:  no 27 = 11011
* * * ![Screenshot from 2022-03-27 11-55-32](https://user-images.githubusercontent.com/25542518/160269469-7ef0a762-c107-423e-b0fb-6cbd70e2b410.png)
* * * ![Screenshot from 2022-03-27 11-55-42](https://user-images.githubusercontent.com/25542518/160269468-ce64d7a5-8f6f-4eee-9c88-6629c27a8a20.png)
* * * ![Screenshot from 2022-03-27 11-55-51](https://user-images.githubusercontent.com/25542518/160269463-5605e638-198c-4dd3-b23d-818d26375388.png)

* Half Adder - Add 2 binary digits
* * 0+0 = 00 (in decimal, this is 0+0=0)
* * 0+1 = 01 (in decimal, this is 0+1=1)
* * 1+0 = 01 (in decimal, this is 1+0=1)
* * 1+1 = 10 (in decimal, this is 1+1=2)
* * This is called a half adder. If our computer can implement this, and if it can chain many of them together, it can add anything.

* * &nbsp;&nbsp;&nbsp;10001111111101
* * \+  00011100111110
* * = 10101100111011

> Adding the qiskit
* part of the circuit that encodes the input, a part that executes the algorithm, and a part that extracts the result.
* barrier
* From Half Adder: The rightmost bit in all four of these answers is completely determined by whether the two bits we are adding are the same or different.
* * In quantum computers, the job of the XOR gate is done by the controlled-NOT gate = CNOT = cx
* * ![Screenshot from 2022-03-27 13-05-46](https://user-images.githubusercontent.com/25542518/160271703-9873b81c-70f1-48b6-9b48-a9e47ffc0f33.png)
* * input bits
* * control qubit .
* * target qubit .+
* * The target becomes 0 if they are the same, and 1 if they are different.
* * _**Another way of explaining the CNOT is to say that it does a NOT on the target if the control is 1, and does nothing otherwise.**_
* * * ![Screenshot from 2022-03-27 13-27-03](https://user-images.githubusercontent.com/25542518/160272479-5e93350f-d43c-4827-bca3-d9ba14fdf9a3.png)
* * * o/p output is 11.
* * * The CNOT sees that qubit 0 is in state 1, and so applies a NOT to qubit 1. This flips the 0 of qubit 1 into a 1, and so turns 01 into 11.
----
> ### 
----

----
> ### 
----
----
> ### 
----
----
> ### 
----
----
> ### 
----
----
> ### 
----
----
> ### 5_QuantumTeleportation
----
transfer  of quantum information from 1 quibit to other


