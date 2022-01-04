# 2D-Heat equation solver

The project is about writing a solver for steady state solution of 2D heat equation.  
Since the steady state solution is time independent, the pde reduces to Poisson equation with right hand side as zero (Laplace equation) and that is what we solve in this project.  
We make use of the finite difference method for solving this.  
We plot our solution using Matlab and compare our results to the solution to analytical result.
For this project, we use the Eigen Librairy for the mathematical operations and for solving the differential equation

# solvers
We made 3 solvers :  
-jacobi_method   
-Gauss-Seidel   
-LU factorisation  

# Tests 
Convergence test example  
Results of convergence test are with respect to inf_norm:  
Boundary values:  
u(x,1) = cos(pi * x)* sinh(pi)
u(0,y) = sinh(pi * y)  
u(x,0) = 0
du(x,y)/dx = 0 (at x = 1)
Analytical Solution: u(x,y) = cos(pi * x)* sinh(pi* y)

# UML Diagram


# Results
![Screenshot 2022-01-02 212630](https://user-images.githubusercontent.com/73020056/147888619-99e38ad6-623b-4c16-8b90-f3cb6196daf9.png)

# Building 
This project was made on Linux, you can run it easily using the Cmakelist.txt.
-Open Terminal in the root of ./build   
  -wrrite "cmake ./src/"  
  -write "make"  
  -./heat_equation_app or ./TEST_Dirichlet or (other tests)
