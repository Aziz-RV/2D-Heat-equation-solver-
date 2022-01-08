
This folder contains the results of the convergence tests:

- We have added the 4 meshes as csv files on which the tests are done. 
	- mesh_1.csv is the mesh with mesh-size hx = hy = 0.2 for a domain of [0,1]^2
	- mesh_2.csv is the mesh with mesh-size hx = hy = 0.1 for a domain of [0,1]^2
	- mesh_3.csv is the mesh with mesh-size hx = hy = 0.05 for a domain of [0,1]^2
	- mesh_4.csv is the mesh with mesh-size hx = hy = 0.025 for a domain of [0,1]^2
	
	These files are used when plotting the solution vector files generated by the test_dirichlett.cpp.
	
We have used these meshes and the resulting vector files to plot the figures inside the Matlab_plot_photos folder. This plotting is done using the plottingfile.m 
The plottingfile also plots the real solution, these too have been added to the Matlab_plot_photos folder.

Lastly, the main result of the test_dirichlett.cpp is the 2-norm errors between the numerical and the analytical solution. 
We have done this for 4 different mesh-sizes and as the mesh-size is halved, the error becomes 1/4th indicating a second order convergence in meshsize.

Details about the convergence test:

The convergence test is meant to check the validity of our implementation. 
The finite difference method solves the steady state heat equation on a 2D square domain.
The test case is on domain [0,1]^2 with meshsize being equal along both x and y direction.
The boundary conditions are as follows:

u(x,0) = 0,

u(0,y) = 0,

u(y,1) = 0,

u(x,1) = sin(pi * x)*sinh(pi)

the analytical solution is u(x,y) = sin(pi * x)*sinh(pi * y)



