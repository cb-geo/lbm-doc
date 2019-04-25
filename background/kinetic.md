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

$$ f^{eq}(\boldsymbol{x},|\boldsymbol{v}|,t)=\rho(\frac{3}{4\pi e})^{3/2} \;\text{e}^{-3|\boldsymbol{v}|^2/(4e)}  $$ 

which is often called the Maxwell-Boltzmann distribution.

## The Boltzmann Equation and the Collision Operator

To study the evolution of the distribution function with time, the total derivative of this function with respect to time can be taken as follows:

$$ \Omega(f)=\frac{df}{dt}=\frac{\partial f}{\partial t}+\xi_{\beta}\frac{\partial f}{\partial x_{\beta}}+\frac{F_{\beta}}{\rho}\frac{\partial f}{\partial \xi_{\beta}} $$

The equation above is called the Boltzmann equation, and $\Omega(f)$ is called the collision operator, which represents the local redistribution of $f$ due to collisions.

Boltzmann's original operator is of the form of a complicated and cumbersome double integral over velocity space. It considers all the possible outcomes of two-particle collisions for any choice of intermolecular forces. Bhatnagar, Gross and Krook have introduced a much simpler collision operator, called the BKG operator, as shown below:

$$ \Omega(f)=-\frac{1}{\tau}(f-f^{eq}) $$

where $\tau$ is the relaxation time which is a function of transport coeficients such as viscosity and heat diffusivity. This equation satisfies the conseravtion of mass and momentum, and ensures that the distribution function $f$ locally evolves towards it equilibrium $f^{eq}$, but it is not as exact as Boltzmann's original operator.

All the macroscopic equations of fluid mechanics can be found from the Boltzmann's equation by taking its moments.

$$ \textbf{Conservation of Mass:} \int{\Omega(f)d^3\xi}=0 $$
$$ \textbf{Conservation of Momentum:} \int{\boldsymbol{\xi}\Omega(f)d^3\xi}=\boldsymbol{0} $$
$$ \textbf{Conservation of Internal Energy:} \int{|\boldsymbol{\xi}|^2\Omega(f)d^3\xi}=0 $$


