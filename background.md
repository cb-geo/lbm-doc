In this section, a background on the most commonly used equations in fluid dynamics is provided.
In these equations which describe the behavior of a fluid, the unknows include density, $\rho$, velocity vector, $\textbf{u}=[u_x,u_y,u_x]$, and the pressure, $p$.

## Conservation of Mass
### Continuity Equation

The continuity equation describes the conservation of mass in fluid dynamics and is expressed as follows:

$$ \frac{\partial \rho}{\partial t}+\nabla.(\rho\mathbf{u})=0 $$

In this equation the vector $\rho\mathbf{u}=\mathbf{j}$ is called the $\textbf{momentum density}$ or $\textbf{mass flux density}$.

## Conservation of Momentum
### Euler Equation

The Euler equation describes the conservation of momentum in an ideal fluid and is expressed as follows:

$$ \frac{\partial(\rho\mathbf{u})}{\partial t}+\nabla.(\rho\mathbf{uu})=-\nabla p + \mathbf{F} $$

where $\textbf{F}$ is the external body force.

This equation can be also written in a more general form:

$$ \frac{\partial(\rho\mathbf{u})}{\partial t}+\nabla.\Pi=\textbf{F} $$

which is called the $\textbf{Cauchy momentum equation}$, where the $\textbf{momentum flux}$ density tensor is defined as:

$$ \Pi_{\alpha\beta}=\rho u_{\alpha}u_{\beta}-\sigma_{\alpha\beta} $$

In this equation $\sigma_{\alpha\beta}$ is the $\textbf{stress tensor}$ which corresponds to the non-direct momentum transfer of the moving fluid.

### Navier-Stokes Equation

Since the Euler equation describes the behavior of ideal fluids, it does not account for energy loss. In real fluids, the momentum will dissipate in tranfer from one fluid element to another, thus, a viscosity term in needed. To this end, the $\textbf{viscous stress tensor $\sigma'$}$ can be defined as follows:

$$ \sigma'_{\alpha\beta}=\eta(\frac{\partial u_{\alpha}}{\partial x_{\beta}}+\frac{\partial u_{\beta}}{\partial x_{\alpha}})+\zeta\delta_{\alpha\beta}\frac{\partial u_{\gamma}}{\partial x_{\gamma}}$$

where $\eta$ and $\zeta$ are the shear and the dilational viscosity coefficients, respectively.

The total stress tensor can be now written as the sum of the pressure and viscosity contirbutions as follows:

$$ \sigma_{\alpha\beta}=\sigma'_{\alpha\beta}-p\delta_{\alpha\beta} $$

Substituting the last two equations in the Cauchy momentum equation, which is the generalized Euler equation, results in the Navier-Stokes equation:

$$ \frac{\partial(\rho u_{\alpha})}{\partial t}+\frac{\partial(\rho u_{\alpha}u_{\beta})}{\partial x_{\beta}}=-\frac{\partial p}{\partial x_{\alpha}}+\frac{\partial}{\partial x_{\beta}}[\eta(\frac{\partial u_{\alpha}}{\partial x_{\beta}}+\frac{\partial u_{\beta}}{\partial x_{\alpha}})+(\eta_B-\frac{2\eta}{3})\frac{\partial u_{\gamma}}{\partial x_{\gamma}}\delta_{\alpha\beta}]+F_{\alpha} $$ 

where $\eta_B = 2\eta/3 +\zeta$ is referred to as the bulk viscosity.

Assuming the viscosities to be constant and the fluid to be incompressible, the well-know incompressible Navier-Stokoes equation can be derived as:

$$ \rho \frac{Du}{Dt}=-\nabla p+\eta\Delta u+ F $$ 

where $\frac{D}{Dt}$ is the material derivative and $\delta$ is the Laplace operator.

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

Using five independent equations that describe the behavior of the fluid, the five unknowns, $\rho$, $u_x, u_y, u_z$, and $p$ can be evaluated. These five equations include: the continuity equation, either Euler or Navier-Stokes equatioin in 3 directions, and one state equation. 
