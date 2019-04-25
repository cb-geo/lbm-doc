# Numerical Methods

Analytical solutions for the equations presented in the previous sections can be obtained only for very limited cases. For most problems, the equtions need to be solved numerically dues to the non-linearities and complex boundary conditions. In this section, a list of the common numerical methods used fro fluid simulations is provided.

## Conventional Navier-Stokes Solvers
These methods take a macroscopic view of the fluid, with the goal of solving the governing differential equations is continuum fluid mechanics.
### The Finite Difference Method (FDM)

In this method, the differential equation is solved by approximating the derivatives using finite differences.<br>
$\textbf{Advantage}$: simple compared to the other conventional method <br>
$\textbf{Disadvantages}$: non-conservative (in terms of mass, momentum, and energy) unless special care is taken, false diffusion even in pure-advection cases, issues with complex geometries

### The Finite Volume Method (FVM)

In this method, the volume integrals in the partial differential equation are converted to surface integrals using divergence theorm.<br>
$\textbf{Advantages}$: fundamentally conservative, complex geometries can be captured well<br>
$\textbf{Disadvantages}$: making the appropriate grid for complex geometries is fairly complex, higher-order FV methods are not straightforward

### The Finite Element Method (FEM)

In this method, the partial differential equation is multiplied by a weight function and integrated over the domain of interest and discretized using basis functions.<br>
$\textbf{Advantages}$: well-equipped for unstructured grid, suitable for increasing the order of accuracy through higher-order basis functions<br>
$\textbf{Disadvantages}$: non-conservative, complex compared to other conventional methods

## Particle Based Solvers
These methods take a microscopic or mesoscopic view of the fluid. The particle, depending on the method, may represent an atom, a molecule, a collection of molecules, or a portion of the macroscopic fluid.
### Molecular Dynamics (MD) [1950s]
In this method, the position of particles (typically atoms or molecule), which interact through intermolecular forces representing the actual physical force, is tracked by numerically integrating Newton's equation of motion.<br>
$\textbf{Advantages}$: great method for simulating microscopic phenomena like chemical reactions <br>
$\textbf{Disadvantages}$: highly impractical as a Navier-Stokes solver due to the large number of molecules in the system

### Lattice Gas Models [1970s-1980s]
In these models, fictitious particles exist on a lattice where they stream forward and collide in a manner that respects conservation of mass and momentum. The first lattice gas model was named HPP after its inventors and used square lattices. Later on, the FHP model was invented which was similaar to HPP except in used triangular lattices; this change gave the model sufficient lattice isotropy to perform fluid simulations.In addition to these two models, there is a number of more complex lattice gas models with various features such as rest particles with zero velocity, additional collisions, and additional higher-speed particles. <br>
$\textbf{It should be noted that the lattice Boltzmann method grew out of the lattice gas model.}$<br>
$\textbf{Advantages}$: reduction of roundoff errors since the major variable in these models is a Boolean type, massively parallelizable <br>
$\textbf{Disadvantagres}$: has problems with isotropy of the Navier-Stokes equation, struggles to reach a high Reynolds number compared to the conventional methods, statistical noise

### Dissipative Particle Dynamics (DPD) [1992]
This method can be considered a course-grained MD method that allows for simulation of larger length and time scales rather than molecular dynamics. The particles in this model are cluster of molecules which interact via three different forces: conservative, dissipative, and random.<br>
$\textbf{Advantages}$: suited for hydrodynamics of complex fluids, such as suspended polymers or biological cell and multiphase flows with complex geometries <br> 
$\textbf{Disadvantages}$: contains a large number of parameters that have to be selected carefully

### Multi-phase Collision (MPC) Dynamics [1999]
I don't know how to explain this one:/<br>
$\textbf{Advantages}$: conserves mass and momentum and has an H-theorem which makes it unconditionally stable, computationally efficient, easy to parallelize, suitable for the simulation of soft mayyer systems <br> 
$\textbf{Disadvantages}$: hard to impose hydrodynamic boundary conditions

### Direct Simulation Monte Carlo (DSMC) [1960s]
This method tracks a large number of statistically representative particles. While the position and velocity of particles is resolved deterministically during motion, particle collisions are approximated by probabilistic, phenomenological models which conserve mass, momentum and energy. <br>
$\textbf{Advantages}$: primary method to solve realistic problems in high Knudsen number flows. <br>
$\textbf{Disadvantages}$: high computational demand

### Smoothed-Particle Hydrodynamics (SPH) [1970s]
This method is an interpolation scheme which uses point particles that influence their vicinity.<br>
$\textbf{Advantages}$: suitable for large unbounded domains with huge density variations and problems with large deformations, perfect conservation of mass and momentum <br>
$\textbf{Disadvantages}$: low accuracy, hard to deal with boundary conditions

