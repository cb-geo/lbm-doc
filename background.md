# Continuum Theory

In this section the most commonly used equations to describe the behavior of a fluid in $\textit{macroscale}$ fluid mechanics is provided.
In these equations, the unknows include density, $\rho$, velocity vector, $\boldsymbol{u}=[u_x,u_y,u_x]$, and the pressure, $p$.

## Conservation of Mass
### Continuity Equation

The continuity equation describes the conservation of mass in fluid dynamics and is expressed as follows:

$$ \frac{\partial \rho}{\partial t}+\nabla.(\rho\boldsymbol{u})=0 $$

In this equation the vector $\rho\boldsymbol{u}=\boldsymbol{j}$ is called the $\textbf{momentum density}$ or $\textbf{mass flux density}$.

## Conservation of Momentum
### Euler Equations

The Euler equations describes the conservation of momentum in an ideal fluid and are expressed as follows:

$$ \frac{\partial(\rho\boldsymbol{u})}{\partial t}+\nabla.(\rho\boldsymbol{uu})=-\nabla p + \boldsymbol{F} $$

where $\boldsymbol{F}$ is the external body force.

These equations can be also written in a more general form:

$$ \frac{\partial(\rho\boldsymbol{u})}{\partial t}+\nabla.\Pi=\boldsymbol{F} $$

which are called the $\textbf{Cauchy momentum equations}$, where the $\textbf{momentum flux}$ density tensor is defined as:

$$ \Pi_{\alpha\beta}=\rho u_{\alpha}u_{\beta}-\sigma_{\alpha\beta} $$

In these equations $\sigma_{\alpha\beta}$ is the $\textbf{stress tensor}$ which corresponds to the non-direct momentum transfer of the moving fluid.

### Navier-Stokes Equations

Since the Euler equations describe the behavior of ideal fluids, it does not account for energy loss. In real fluids, the momentum will dissipate in tranfer from one fluid element to another, thus, a viscosity term in needed. To this end, the $\textbf{viscous stress tensor $\sigma'$}$ can be defined as follows:

$$ \sigma'_{\alpha\beta}=\eta(\frac{\partial u_{\alpha}}{\partial x_{\beta}}+\frac{\partial u_{\beta}}{\partial x_{\alpha}})+\zeta\delta_{\alpha\beta}\frac{\partial u_{\gamma}}{\partial x_{\gamma}}$$

where $\eta$ and $\zeta$ are the shear and the dilational viscosity coefficients, respectively.

The total stress tensor can be now written as the sum of the pressure and viscosity contirbutions as follows:

$$ \sigma_{\alpha\beta}=\sigma'_{\alpha\beta}-p\delta_{\alpha\beta} $$

Substituting the last two equations in the Cauchy momentum equations, which is the generalized Euler equations, results in the Navier-Stokes equations:

$$ \frac{\partial(\rho u_{\alpha})}{\partial t}+\frac{\partial(\rho u_{\alpha}u_{\beta})}{\partial x_{\beta}}=-\frac{\partial p}{\partial x_{\alpha}}+\frac{\partial}{\partial x_{\beta}}[\eta(\frac{\partial u_{\alpha}}{\partial x_{\beta}}+\frac{\partial u_{\beta}}{\partial x_{\alpha}})+(\eta_B-\frac{2\eta}{3})\frac{\partial u_{\gamma}}{\partial x_{\gamma}}\delta_{\alpha\beta}]+F_{\alpha} $$ 

where $\eta_B = 2\eta/3 +\zeta$ is referred to as the bulk viscosity.

Assuming the viscosities to be constant and the fluid to be incompressible, the well-known incompressible Navier-Stokoes equations can be derived as:

$$ \rho \frac{D\boldsymbol{u}}{Dt}=-\nabla p+\eta\Delta \boldsymbol{u} +\boldsymbol{F} $$ 

where $\frac{D}{Dt}$ is the material derivative and $\Delta$ is the Laplace operator.

## State Principle
### Equation of State

The state principle of equilibrium thermodynamics declares that any of the state variables, such as the density, $\rho$, the pressure, $p$, the temperature, $T$, the internal energy, $e$, and the entropy, $s$, can be related to any other two state variables through an equation of state. Below is a list of the most commonly used equation of states:

$\textbf{The ideal gas law}$:

$$ p=\rho RT $$

$ \textbf{The isentropic equation of state}$, which assumes constant entropy:

$$ p=p_0(\frac{\rho}{\rho_0})^{\gamma} $$

$ \textbf{The isothermal equation of state}$, which assumes constant temprature:

$$ p=\rho RT_0 $$

<br/><br/>

Using five independent equations that describe the behavior of the fluid, the five unknowns, $\rho$, $u_x, u_y, u_z$, and $p$ can be evaluated. These five equations include: the continuity equation, either Euler or Navier-Stokes equations (3 equations dues to the 3 directions), and a state equation.

# Kinetic Theory 

In this section, a summary of kinetic theory, which describes the behavior of a fluid in the $\textit{mesoscopic}$ scale, is provided.

## The Distribution Function

The particle $\textbf{distribution fucntion}$, $f(\boldsymbol{x},\boldsymbol{\xi},t)$ is the fundamental variable in kinetic theory, which represents the density of the mass in both three-dimensional physical space ($\boldsymbol{x}$) and three-dimentional particle velocity space ($\boldsymbol{\xi}$), and has the unit $kg/(m^3)/(m/s)^3=\frac{kgs^3}{m^6}$. In other words, the distribution function $f(\boldsymbol{x},\boldsymbol{\xi},t)$ represents the density of particles with velocity $\boldsymbol{\xi}=[\xi_x,\xi_y,\xi_z]$ at position $\boldsymbol{x}$ and time $t$.

The macroscopic variables such as mass density, $\rho$, momentum density, $\rho\boldsymbol{u}$, total energy density $\rho E$, and internal energy density, $\rho e$, can be calculated using the moments of the distribution function as follows:

$$ \rho(\boldsymbol{x},t)=\int{f(\boldsymbol{x},\boldsymbol{\xi},t)d^3\xi} $$
$$ \rho(\boldsymbol{x},t)\boldsymbol{u}(\boldsymbol{x},t)=\int{\boldsymbol{\xi}f(\boldsymbol{x},\boldsymbol{\xi},t)d^3\xi} $$
$$ \rho(\boldsymbol{x},t)E(\boldsymbol{x},t)=\frac{1}{2}\int{|\boldsymbol{\xi}|^2f(\boldsymbol{x},\boldsymbol{\xi},t)d^3\xi} $$
$$ \rho(\boldsymbol{x},t)e(\boldsymbol{x},t)=\frac{1}{2}\int{|\boldsymbol{v}|^2f(\boldsymbol{x},\boldsymbol{\xi},t)d^3\xi} $$

where in the last equation $v(\boldsymbol{x},t)=\boldsymbol{\xi}(\boldsymbol{x},t)-\boldsymbol{u}(\boldsymbol{x},t)$is the $\textbf{relative velocity}$.

The macroscoopic pressure can be also found using the equipartition theorem of classical statistical mechanics, the ideal gas law, and the internal energy density derived above:

$$ p=\rho RT=\frac{2}{3}\rho e=\frac{1}{3}\int{|\boldsymbol{v}|^2f(\boldsymbol{x},\boldsymbol{\xi},t)d^3 \xi} $$

## The Equilibrium Distribution Function

When a gas has been left alone for sufficiently long, the particle collisions tend to even out the angular distribution of particle velocities around the mean velocity $\boldsymbol{u}$, so it may be assumed that the distribution function will reach an equilibrium distribution $f^{eq}(\boldsymbol{x},\boldsymbol{\xi},t)$ which is isotropic in velocity space around $\boldsymbol{\xi}=\boldsymbol{u}$. In a reference frame moving with speed $\boldsymbol{u}$, the equilibrium distribution can be derived as:

$$ f^{eq}(\boldsymbol{x},|\boldsymbol{v}|,t)=\rho(\frac{3}{4\pi e})^{3/2} e^{-3|\boldsymbol{v}|^2/(4e)}  $$ 

which is often called the Maxwell-Boltzmann distribution.

## The Boltzmann Equation

To study the evolution of the distribution function with time, the total derivative of this function with respect to time can be taken as follows:

$$ \Omega(f)=\frac{df}{dt}=\frac{\partial f}{\partial t}+\xi_{\beta}\frac{\partial f}{\partial x_{\beta}}+\frac{F_{\beta}}{\rho}\frac{\partial f}{\partial \xi_{\beta}} $$

The equation above is called the Boltzmann equation, and $\Omega(f)$ is called the collision operator, which represents the local redistribution of $f$ due to collisions.

Boltzmann's original operator is very complicated. Bhatnagar, Gross and Krook have introduced a much simpler collision operator, called the BKG operator, as shown below:

$$ \Omega(f)=-\frac{1}{\tau}(f-f^{eq}) $$

where $\tau$ is the relaxation time which is a function of transport coeeficients such as viscosity and heat diffusivity. This equation satisfies the conseravtion of mass and momentum, and ensures that the distribution function $f$ locally evolves towards it equilibrium $f^{eq}$, but it is not as exact as Boltzmann's original operator.
