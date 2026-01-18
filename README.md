# laminar_BL_openFoam
Laminar boundary layer solution using OpenFoam's icoFoam solver.

Boundary condition in the U file are:

Constant Velocity (Dirichlet) b.c. is used for the (left side) inlet
zeroGradient (Neumann) b.c. is used on the outlet (right side)
zeroGradient (Neumann) b.c. is used on the freestream & the bottom
noSlip b.c. for the flat plate
