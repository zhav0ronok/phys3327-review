*Note: I will take this page down once the exam has been graded! It is just useful to have up in the meantime.*
### External Resources
- [Desmos Graphing Calculator](https://www.desmos.com/calculator)
- [Integral Calculator]([https://www.integral-calculator.com](https://www.integral-calculator.com/))
- **Lecture Notes (on Canvas); MOST USEFUL!!!** 
- All previous problem set solutions
- Heald & Marion (Third Edition)
- Practice Prelim soln's
---
### Useful Equations
**Law of Cosines:**
$$
R = r^2 + a^2 -  2ar \cos(\theta)
$$
**Some vector calculus identities:**
$$  
\nabla \cdot (\nabla \times \mathbf{A}) = 0  
\\ 
\nabla \times (\nabla \Phi) = 0  
\\\\ 
\nabla \cdot (\Phi \mathbf{A}) = \Phi(\nabla \cdot \mathbf{A}) + \mathbf{A} \cdot \nabla \Phi  
\\ 
\nabla \times (\Phi \mathbf{A}) = \Phi(\nabla \times \mathbf{A}) + \nabla \Phi \times \mathbf{A}  
\\ \\
\nabla \cdot (\mathbf{A} \times \mathbf{B}) = \mathbf{B} \cdot (\nabla \times \mathbf{A}) - \mathbf{A} \cdot (\nabla \times \mathbf{B})  
\\
\nabla \times (\mathbf{A} \times \mathbf{B}) = \mathbf{A}(\nabla \cdot \mathbf{B}) - \mathbf{B}(\nabla \cdot \mathbf{A}) + (\mathbf{B} \cdot \nabla)\mathbf{A} - (\mathbf{A} \cdot \nabla)\mathbf{B}  
\\ \\
\nabla^2 \Phi = \nabla \cdot (\nabla \Phi)  
\\
\nabla^2 \mathbf{A} = \nabla(\nabla \cdot \mathbf{A}) - \nabla \times (\nabla \times \mathbf{A})  
$$

**Useful integrals/integral theorems:**
$$
\int_{-1}^1 (x^2-1) \cos\left(  \frac{(2n-1)\pi}{2}x \right)dx = (-1)^n \frac{32}{(2n-1)^3 \pi^3}
$$
$$  
\int_V (\nabla \cdot \mathbf{A})d^3x = \oint_S \mathbf{A} \cdot d\mathbf{a}  

\\  
\int_S (\nabla \times \mathbf{A}) \cdot d\mathbf{a} = \oint_C \mathbf{A} \cdot d\mathbf{l}  
\\
\int_V \nabla \Phi,d^3x = \oint_S \Phi,d\mathbf{a}  
$$
**Some Fourier expansions:**
For an even function,
$$  
f(x)=\sum_{n=0}^{\infty}a_n\cos\left(\frac{n\pi x}{L}\right)  
$$
with
$$  
a_n=\frac{1}{L}\int_{-L}^{L}f(x)\cos\left(\frac{n\pi x}{L}\right),dx  
$$
For an odd function,
$$  
f(x)=\sum_{n=1}^{\infty}b_n\sin\left(\frac{n\pi x}{L}\right)  
$$
with
$$  
b_n=\frac{1}{L}\int_{-L}^{L}f(x)\sin\left(\frac{n\pi x}{L}\right),dx  
$$

---
# General Notes

### Maxwell's Equations

##### Gaussian Units
$$
\begin{align}
&\text{Gauss's Law (Electricity):} &\nabla \cdot \mathbf{E} = 4\pi \rho\\&\text{Gauss's Law (Magnetism):}&\nabla \cdot \mathbf{B} = 0\\ &\text{Faraday's Law:}&\nabla \times \mathbf{E} = -\frac{1}{c} \partial_{t} \mathbf{B}\\ &\text{Ampere-Maxwell Law:}&\nabla \times \mathbf{B} = \frac{4\pi}{c} \mathbf{J} + \frac{1}{c} \partial_{t} \mathbf{E}

\end{align}
 $$
 ##### SI Units
$$
 \nabla \cdot \mathbf{E} = \frac{\rho}{\epsilon_{0}}\\\nabla \cdot \mathbf{B}=0\\ \nabla \times \mathbf{E} = -\partial_{t}\mathbf{B}\\ \nabla \times \mathbf{B} = -\mu_{0} \mathbf{J} + \mu_{0}\epsilon_{0} \partial_{t} \mathbf{E}
 $$
### Multipole Expansion

The general multipole expansion
$$
\Phi(r,\phi,\theta) = \sum_{l=0}^\infty \frac{1}{2l+1} \sum_{m=-l}^l q_{lm} (\rho(\vec{x}))Y_{lm}(\theta,\phi) \frac{1}{r^{l+1}}\\
\sim c \frac{R^l}{r^{l+1}}
$$
Where 
$$
q_{lm} = \int d^3 x x^l Y^*_{lm} (\theta_{x}\phi_{x})\rho(x)
$$
##### Far field limit
Only the $1/r$ term survives, as every other term falls off too quickly. 

For $l=0$, we have the **monopole**, and its "moment" is:
$$
Q = \int \rho(r') d^3r'\hspace{.5cm} \Phi \sim \frac{1}{r}
$$
More specifically, from Heald and Marion,
$$
\Phi \equiv \sum_{\alpha} \frac{q_{\alpha}}{r} = \boxed{ \frac{q}{r}}
$$
For $l=1$, we have a **dipole**, and its moment is:
$$
\mathbf{p} = \int r' \rho(r') d^3 r'\hspace{.5cm} \Phi \sim \frac{1}{r^2}
$$

### Boundary Conditions
#### Types of Boundary Conditions
##### Dirichlet Boundary Conditions
The *value of the function* at the boundary is specified
$$
\Phi|_{boundary}= \phi_{0}
$$
##### Neumann Boundary Conditions
The *normal derivative of the function* is specified at the boundary
$$
\frac{\partial\Phi}{\partial n}|_{boun dary} = f
$$
For electrostatics, since $\mathbf{E } = -\nabla \Phi$, this is $-E_n$

#### Properties
##### Superposition
Given
$$
\nabla^2\phi =0
$$
If $\phi_{1}$ and $\phi_{2}$ are both solutions, then the linear combination of them will also be a solution
$$
\phi = a \phi_{1}+b \phi_{2}
$$
##### Smoothness
In one dimension, this diffeq is $\phi’’=0$, which means that $\phi$ has no maximum or minimum. Note that the *boundary* can still have maxima or minima. 
##### Uniqueness
If we have some solution $\phi = \phi_{1}+\phi_{2}$, and the boundaries are set (such that the solution satisfies them), $\phi|_{boundary} = 0\Rightarrow \phi(r)=0$, we may conclude by contradiction that 

#### Laplace Equation
##### In Spherical Coordinates
$$
\partial^2 \Phi = \frac{1}{r^2 } \frac{\partial}{\partial r} \left(  r^2 \frac{\partial\Phi}{\partial r} \right) + \frac{1}{r^2 \sin \theta} \frac{\partial}{\partial \theta} \left( \sin \theta \frac{{\partial \Phi}}{\partial \theta} \right) + \frac{1}{r^2\sin^2\theta}  \frac{\partial^2\Phi}{\partial \phi^2}
$$
The separated solutions have radial dependence:
$$
\Rightarrow R_{l}(r) = A_{l}r^l + B_{l} r^{-(l+1)}
$$

##### In Cylindrical Coordinate
$$
\nabla^2 \Phi = \frac{1}{r} \frac{\partial}{\partial r} \left(  r \frac{\partial\Phi}{\partial r} \right) + \frac{1}{r^2} \frac{{\partial^2 \Phi}}{\partial \phi^2} + \frac{\partial^2\Phi}{\partial z^2}
$$
Separated solution: $\Phi = R(r) \Theta (\phi)Z(z)$

#### Poisson's Equation
In Gaussian units,
$$  
\nabla^2\Phi=-4\pi\rho  
$$
In SI units,

$$  
\nabla^2\Phi=-\frac{\rho}{\epsilon_0}  
$$
In Heaviside-Lorentz (HL) units,

$$  
\nabla^2\Phi=-\rho  
$$

In a charge-free region, $(\rho=0)$, so Poisson's equation reduces to Laplace's equation:
$$  
\nabla^2\Phi=0  
$$
### Method of Images
The method of images is a technique for solving electrostatic boundary-value problems involving conductors. Instead of directly calculating the complicated distribution of induced charge on a conductor, we replace the effect with carefully placed fictitious point charges. These imaginary charges can reproduce the exact electric potential and field in a physical region that we care about. 

The positive point charge has the following equation and solution for Poisson's equation:
$$
\nabla^2 \Phi = -[q \delta (\vec{r} - \vec{r}_{0})] \Rightarrow \Phi(\vec{r}) = \frac{q}{4\pi | \vec{r}-\vec{r}_{0}|}
$$
This works when charges are in space (superimpose them to find total potential), but now imagine placing this charge near the conductor. The charge attracts electrons in the conductor **producing nonuniform induced surface charge density $\sigma(\vec{r})$**. Instead of working through a nasty integral for induced tsurface charge, we can use the method of images!

You may **find fictitious charges whose potential automatically satisfies the appropriate boundary conditions** (uniqueness theorem makes this works out, since if the charge density throughout a region and the electric potential on its entire boundary are specified, there is at most one solution for the electric potential in that region)

A good example is with a *hollow conducting spherical shell of radius $R$*, with a point charge inside the shell.

### Maxwell Stress Tensor $T_{ij}$
In Gaussian units,
$$  
T_{ij}=\frac{1}{4\pi}\left(E_iE_j+B_iB_j-\frac{1}{2}\delta_{ij}(E^2+B^2)\right)  
$$
The electromagnetic momentum density is
$$  
\mathbf{g}=\frac{1}{4\pi c}\mathbf{E}\times\mathbf{B}  
$$
Local momentum conservation can be written as
$$  
\mathbf{f}=\nabla\cdot\mathbf{T}-\frac{\partial\mathbf{g}}{\partial t}  
$$
where $(\mathbf{f})$ is the electromagnetic force per unit volume on matter.
Integrating over a volume $(V)$,
$$
 \oint_S \mathbf{T}\cdot d\mathbf{a}
\to\frac{d}{dt}\int_V\mathbf{g}\;d^3x  $$

The surface integral gives the net electromagnetic stress acting on the volume. In a source-free region, the tensor satisfies
$$  
\nabla\cdot\mathbf{T}=\frac{\partial\mathbf{g}}{\partial t}  
$$
For a static electromagnetic field in vacuum, where $(\partial_t\mathbf{g}=0),$

$$  
\nabla\cdot\mathbf{T}=0  
$$
### EM Waves and Polarization
A general monochromatic, completely polarized plane wave traveling in the $z$ direction can be written as
$$
\vec{E}(z,t) = E_{x} \hat{x} \exp[i(kz - \omega t + \phi_{x}) ] + E_{y} \hat{y} \exp[i(kz-\omega t + \phi_{y})]
$$
In a circular basis, it is
$$
\vec{E}(z,t) = E_{L} \hat{L} \exp[i(kz - \omega t + \phi_{L}) ] + E_{R} \hat{R} \exp[i(kz-\omega t + \phi_{R})]
$$
Where $\hat{R} = \frac{\hat{x} + i\hat{y}}{\sqrt{ 2 }}$ and $\hat{L} = \frac{\hat{x} - i\hat{y}}{\sqrt{ 2 }}$ and $E_{L},E_{R} \in \mathbb{R}$


---
# Specific Cases
## Multipole Examples
The general multipole approach is (1) identify the source charges/charge density, (2) calculate the total charge $Q$, (3) if $Q=0$, calculate the dipole moment, (4) if the dipole also vanishes, calculate the next nonzero moment.

#### Dipole
*Heald and Marion page 43*

The setup is a positive and negative charge of equal magnitude along one axis, each a distance $l$ from the origin, and a point $P$ which has a location described by a vector $\vec{r}$ originating at $O$. 

The potential at a point $P(r,\theta,\phi)$ is given by
$$
\Phi = q \left(  \frac{1}{R_{1}} - \frac{1}{R_{2}} \right) \sim\frac{ 2ql \cos \theta}{r^2}
$$
Where $R_1$ is the distance from the first charge ($q+$) to $P$ and $R_{2}$ from $q-$. It is approximated using the law of cosines. 

The dipole moment is:
$$
\mathbf{p} \equiv 2ql \mathbf{e}
$$
Where $\mathbf{e}$ is the unit vector pointing along $\vec{r}$. The dipole potential can also be expressed as 
$$
\Phi = \frac{\mathbf{p}\cdot \mathbf{e}}{r^2}
$$

The dipole electric field is
$$
\mathbf{E}_{dip} = \frac{1}{4\pi \epsilon_{0} r^3} [ 3(\mathbf{p} \cdot \mathbf{\hat{r}})\mathbf{\hat{r}}- \mathbf{p}]
$$
And in spherical coordinates with the dipole along $z$ (in Gaussian units):
$$
\begin{align}
E_{r} = \frac{2p \cos \theta}{4\pi \epsilon_{0}r^3}\\  E_{\theta} =\frac{ p \sin\theta}{4\pi \epsilon_{0}r^3}\\ E_{\phi} = 0
\end{align}
$$
Note: Heald and Marion does not use gaussian units, so you can just remove the $1 / 4\pi \epsilon_{0}$ factor
#### Quadrupole
*From problem set 3:*
![[Pasted image 20261022172501.png]]
$$
T_{ij} = \frac{\partial^2}{\partial x_{i}\partial x_{j}}\left(  \frac{1}{r} \right) = \frac{3 \hat{r}_{i}\hat{r}_{j} - \delta_{ij } }{r^3}
$$

#### Square tunnel
*From problem set 5*
![[Pasted image 20261022173616.png]]

The general solution is
$$
\Phi(x,y) = \sum \Phi_{n}(x,y)
$$
Where
$$
\Phi_{n}(x,y) = (a_{n}e^{\beta_{n}y}+ b_{n}e^{-\beta_{n}y}) \cos \beta_{n}x + (c_{n}e^{\alpha_{n}y}+ d_{n}e^{-\alpha_{n }y})\sin\alpha_{n}x
$$
With 
$$
\beta_{n} = \frac{(2n-1)\pi}{2L} \hspace{.5cm} \alpha_{n} = \frac{n\pi}{L}
$$

If $f(x)$ is even, $c_n=d_n=0$ and the other cofficients are unconstrained. If $f$ is odd, the opposite is true.

___

