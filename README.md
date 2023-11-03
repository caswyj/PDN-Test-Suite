# PDN-Test-Suite
This repository contains Power Delivery Network(PDN) circuits for performance test. 
For ease of use, the system matrix C and G of the PDNs are provided.
The Differential-Algebraic-Equation(DAE) for transient analysis of a PDN is as follows:
$$C\frac{dx}{dt}+Gx=b(t),$$
$$x(0)=x_0.$$
Therefore, for a specififc PDN, it is only necessary to provide $C,G$. The source term $b(t)$
can be easily defined by the users.
In this test suite, PDN matrices are all generated from real netlists drawn from industrial design
and test cases. Researchers can take this test suite as a benchmark library for state-of-the-art PDN 
simulation algorithms. If you like our test suite, please star our project, thank you very much. 
If you have any issues, please start an Issue on this project.  
For example, in pg1/, dQdx.mtx stores the matrix $C$ data, while dFdx.mtx stores the matrix $G$ data.
dQdx_add_diag.mtx adds random values on the diagonal of matrix $C$ which ensures the matrix is invertible
(in real circuits, $C$s are generally rank-deficient, this add value operation is simply for ease of use 
 in some test situations).
