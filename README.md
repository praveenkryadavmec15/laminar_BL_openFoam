Laminar Boundary Layer over Flat Plate (icoFoam)

Laminar incompressible boundary layer verification case using OpenFOAM's icoFoam solver. Validates against Blasius analytical solution. Domain: 0.6m × 0.1m (scale=0.1), 0.1m entrance + 0.5m plate.

Case Geometry

    Total length: 0.6 m (scale 0.1 × 6 units)

    Entrance region: 0.1 m (x=0→0.1, freestream bottom)

    Plate length: 0.5 m (x=0.1→0.6, noSlip wall)

    Height: 0.1 m (~2% blockage ratio)

Boundary Conditions - 0/U File (Written Form)

The velocity boundary conditions in the 0/U file are specified as follows:

For the inlet patch (left side entrance at x=0): type fixedValue with value uniform (1 0 0), representing constant freestream velocity U∞=1 m/s in the x-direction (Dirichlet condition).

For the outlet patch (right side exit at x=0.6m): type zeroGradient, allowing fully developed flow to exit without gradient constraint (Neumann condition).

For the freestream patch (top wall and entrance sidewalls): type fixedValue with value uniform (1 0 0), maintaining freestream conditions along domain boundaries.

For the entrance_bottom patch (bottom wall from x=0 to 0.1m before plate): type fixedValue with value uniform (1 0 0), representing undisturbed freestream before boundary layer development.

For the plate patch (flat plate surface from x=0.1 to 0.6m): type noSlip, enforcing zero velocity (u=0, v=0) at the wall.

For the frontAndBack patches: type empty for 2D simulation approximation.
Boundary Conditions - 0/p File

Pressure boundary conditions complement velocity BCs: zeroGradient on inlet, freestream, entrance_bottom, and plate patches; fixedValue uniform 0 on outlet (reference pressure); empty on frontAndBack.
