2DNLH
=====

Code for solution of the scalar Nonlinear Helmholtz equation for modeling collapsing optical beams.

These files contain Matlab code for solving the Nonlinear Helmholtz equation
for collapsing optical beams, as published in:
G. Baruch, G. Fibich, S.V. Tsynkov: ``High-Order Numerical Solution of the Nonlinear Helmholtz Equation in Multidimensional Layered Media'', J. of Comp.  Physics, 228 (10), 2009 pp. 3789-3815.
G. Baruch, G. Fibich, S.V. Tsynkov: ``Simulations of the Nonlinear Helmholtz Equation: Arrest of Beam Collapse, Nonparaxial Solitons, and Counter-Propagating Beams'', Optics Express, 16 (17), pp.13323-13329 (2008).

Permission is granted to use or modify the code freely, but without any
warranty. If this code was used to aid a scientific publication, please cite
our JCP and Optics Express papers above.


The repository contains four directories:
./run  An empty directory holding the results of a run.
./freezing_nlh  Holding a reference implementation of the freezing-iteration
schemes. The reader may benefit from understanding this simpler code before
the more involved Newton code. 
./newton  Holding the Newton solver, including the Jacobian and iteration code.
./shared  Holding shared code between the fixed-point freezing method and the 
Newton solver. Mostly definitions of the linear operator, and some utils.
./shared/longitudinal  Holding definition of the longitudinal Laplacian
./shared/transverse  Holding definition of the transverse Laplacian

The code stores all parameters, variables and operators in the global structure
T.
To run the freezing code: cd to the freezing_nlh subdir and run the matlab
routine freezing_NLH.
To run the Newton code: cd to the newton subdirectory, optionally modify run
parameters at the file newton_params.m, and run the matlab routine newton_NLH.
See the code for explanation of the different parameters.

Author: Guy Baruch mailto:guy.baruch@gmail.com
