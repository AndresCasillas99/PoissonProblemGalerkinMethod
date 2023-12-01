# PoissonProblemGalerkinMethod
 We aim to approximate the solution of the weak form of the Poisson problem in the unit square with zero boundary values using the Galerkin method. It includes plots to visualize approximate solutions for different partition values as well as computations for the erorr terms.  

Concretely, we aim to solve the problem

$\quad u \in V: \quad \int_{\Omega} \nabla u \cdot \nabla v  = \int_{\Omega} f v , \quad\forall v \in V,$

where $\Omega = (0,1)^{2}$ and $V = H_{0}^{1}(\Omega)$. We will use the Galerkin method, which consists in choosing a finite-dimensional subspace $V_{N} \subset V$ and solving 

$\quad u_{N} \in V_{N}: \quad \int_{\Omega} \nabla u_{N} \cdot \nabla v = \int_{\Omega} f v, \quad \forall v \in V_{N}$.

Given $n > 1$, we consider the uniform grid on $\Omega$ with $(n-1)^{2}$ interior nodes and define 

$\qquad V_{N} := <{\phi_{i,j} : i,j = \{1,\dots,n-1\}}>$

where $\phi_{i,j}(x,y) := \psi_{i}(x) \psi_{j}(y)$ and $\psi$ denote the hat functions in $(0,1)$.

We then solve the linear system $Au = Mb$ with the usual stiffness and mass matrices, and compare our solutions with the analytic solutions given by 

$f(x,y) = 5 \pi^{2} sin(2\pi x) sin(xy) \qquad u(x,y) = sin(2\pi x)sin(\pi y)$ 

by computing 

$\lVert u - u_{N} \rVert_{L^{2}(\Omega)}$ and $|u - u_{N}|_{H^{1}(\Omega)}$.

