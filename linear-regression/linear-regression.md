# Linear Regression

**1.when A and B are similar, are A and B have the same eigenvalue?** 

similar matrix of A means that $$B=T^{-1}AT$$ , then $$B\vec v=T^{-1}AT\vec v=>TB\vec v=AT\vec v =>T(\lambda\vec v)=\lambda(T\vec v)=A(T\vec v)$$, then A and B have the same eigenvalue 

**2. Regarding singular values of matrices, the following statements are corrected?**

* [ ] The singular value only exists in the squared matrix
* [ ] The singular value may be positive or negative
* [x] The number of non-zero singular values is related to the rank of the matrix

**3. Sum of two invertible matrice are invertible or not? what about the product of two invertible matrice?** 

Sum of two invertible matrice may not invertible. For example A+\(-A\) = 0; product of 2 invertible matrice are invertible. 

**4. What is the difference between matrix invertibility and diagonalizability? is a diagonalized matrix can be invertible?**

invertibility is concerned with the eigenvalues are zero or not, and diagonalizability is concerned with the eigenvectors too few or equal to rank. 

5. what the relationship between $$rank(A^TA) \text{ and  } rank(A)$$?

$$rank(A^TA)=rank(A)$$.because $$rank(A^TA) = n-dim(Null(A^TA))$$ , rank\(A\)=n-dim\(Null\(A\)\), then for $$x\in Null(A), Ax=0, \text{then } A^TAx=0$$ , so $$x\in Null(A^TA)$$   
if $$x\in Null(A^TA)$$, then $$A^TAx=0, \text{then } x^TA^TAx=0, $$so $$x\in Null(A)$$, we can conclude that $$Null(A^TA) \text{ and }Null(A) $$bijection.

































