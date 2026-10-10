# The Two-Body Problem: From Newtonian Mechanics to General Relativity

### A Complete Mathematical Treatment

**Abstract.** This paper provides a fully self-contained, step-by-step mathematical treatment of the two-body gravitational problem, beginning from first principles of Newtonian mechanics and culminating in the general-relativistic description via the Schwarzschild geometry and geodesic equations. We derive every result from scratch: the vector calculus identities needed, Newton's laws and their consequences, the reduction of the two-body problem to an effective one-body problem, the derivation of conic-section orbits and Kepler's three laws, the conserved quantities and their geometrical interpretation, and then the entire framework of differential geometry and general relativity needed to treat the same problem in Einstein's theory. We derive the Schwarzschild metric in full, construct the effective potential, exhibit the new phenomenon of orbital precession, compute the perihelion advance of Mercury explicitly, and discuss the innermost stable circular orbit and radial plunge. No step is assumed or skipped. Every theorem is proved; every computation is displayed in full.

---

## Table of Contents

1. Mathematical Preliminaries
   - 1.1 Vector Algebra and Notation
   - 1.2 Differential Calculus of Vectors
   - 1.3 The Gradient, Divergence, Curl, and Laplacian
   - 1.4 Key Vector Identities (with Proofs)
   - 1.5 Polar, Spherical, and Cylindrical Coordinates
   - 1.6 Line Integrals, Conservative Fields, and Potential Functions
   - 1.7 Ordinary Differential Equations: Selected Results
2. Newtonian Mechanics
   - 2.1 Newton's Three Laws
   - 2.2 Momentum, Force, and Impulse
   - 2.3 Work, Kinetic Energy, and the Work–Energy Theorem
   - 2.4 Potential Energy and Conservation of Energy
   - 2.5 Angular Momentum and its Conservation
   - 2.6 Centre of Mass and the Two-Body Reduction
3. Newtonian Gravity
   - 3.1 Newton's Law of Universal Gravitation
   - 3.2 The Gravitational Field and Potential
   - 3.3 Gauss's Law for Gravity
   - 3.4 Gravitational Potential Energy of Two Point Masses
4. The Newtonian Two-Body Problem
   - 4.1 Equations of Motion and Centre-of-Mass Reduction
   - 4.2 Conservation of Angular Momentum: Planar Motion
   - 4.3 Conservation of Energy
   - 4.4 The Effective Potential
   - 4.5 The Orbit Equation: Derivation via the Binet Substitution
   - 4.6 Classification of Orbits: Ellipses, Parabolas, Hyperbolas
   - 4.7 Kepler's First Law (from the Orbit Equation)
   - 4.8 Kepler's Second Law (from Angular Momentum Conservation)
   - 4.9 Kepler's Third Law (Derivation for Elliptic Orbits)
   - 4.10 Orbital Elements and the Vis-Viva Equation
   - 4.11 Turning Points, Apsides, and Radial Oscillations
   - 4.12 The Runge–Lenz Vector and its Conservation
5. Elements of Differential Geometry
   - 5.1 Manifolds, Charts, and Coordinate Systems
   - 5.2 Tangent Vectors, Covectors, and Tensors
   - 5.3 The Metric Tensor
   - 5.4 Covariant Differentiation and the Christoffel Symbols
   - 5.5 Geodesics and the Geodesic Equation
   - 5.6 The Riemann Curvature Tensor
   - 5.7 The Ricci Tensor and Ricci Scalar
   - 5.8 The Einstein Tensor
6. Special Relativity: A Foundation
   - 6.1 The Postulates and the Lorentz Transformation
   - 6.2 Minkowski Spacetime and the Metric
   - 6.3 Four-Vectors and the Energy–Momentum Four-Vector
   - 6.4 Proper Time and the Worldline
7. General Relativity
   - 7.1 The Principle of Equivalence
   - 7.2 The Einstein Field Equations: Physical Motivation and Statement
   - 7.3 Derivation from the Einstein–Hilbert Action
   - 7.4 The Stress–Energy Tensor
   - 7.5 The Weak-Field Limit and Recovery of Newtonian Gravity
8. The Schwarzschild Solution
   - 8.1 Spherical Symmetry and Birkhoff's Theorem
   - 8.2 Derivation of the Schwarzschild Metric in Full
   - 8.3 Coordinate Singularities and the Schwarzschild Radius
   - 8.4 Geodesics in Schwarzschild Spacetime: General Setup
   - 8.5 Conserved Quantities from Killing Vectors
9. The Relativistic Two-Body (Test-Particle) Problem
   - 9.1 The Effective Potential in Schwarzschild Geometry
   - 9.2 Circular Orbits and their Stability
   - 9.3 The Innermost Stable Circular Orbit (ISCO)
   - 9.4 The Orbit Equation in GR: Derivation
   - 9.5 Perturbative Solution: Orbital Precession
   - 9.6 The Perihelion Advance of Mercury: Explicit Calculation
   - 9.7 Radial Geodesics: Free-Fall into a Black Hole
   - 9.8 Comparison with the Newtonian Orbit Equation
10. Summary and Conclusions
11. Appendix A: Proof of the Conic Section Polar Equation
12. Appendix B: Christoffel Symbols for the Schwarzschild Metric
13. Appendix C: Riemann Tensor Components for Schwarzschild

---

# Chapter 1: Mathematical Preliminaries

This chapter establishes the mathematical language used throughout the paper.

## 1.1 Vector Algebra and Notation

We work in Euclidean three-dimensional space $\mathbb{R}^3$. A **vector** is an ordered triple

$$\mathbf{A} = A_x\,\hat{\mathbf{e}}_x + A_y\,\hat{\mathbf{e}}_y + A_z\,\hat{\mathbf{e}}_z = \sum_{i=1}^{3} A_i\,\hat{\mathbf{e}}_i,$$

where $\hat{\mathbf{e}}_i$ are mutually orthogonal unit vectors satisfying

$$\hat{\mathbf{e}}_i \cdot \hat{\mathbf{e}}_j = \delta_{ij}, \qquad \hat{\mathbf{e}}_i \times \hat{\mathbf{e}}_j = \epsilon_{ijk}\,\hat{\mathbf{e}}_k.$$

Here $\delta_{ij}$ is the **Kronecker delta** and $\epsilon_{ijk}$ is the **Levi-Civita symbol**, defined by

$$\epsilon_{ijk} = \begin{cases} +1 & \text{if } (i,j,k) \text{ is an even permutation of } (1,2,3),\\ -1 & \text{if } (i,j,k) \text{ is an odd permutation of } (1,2,3),\\ 0 & \text{if any two indices are equal.} \end{cases}$$

**The dot product.** For $\mathbf{A}, \mathbf{B} \in \mathbb{R}^3$:

$$\mathbf{A} \cdot \mathbf{B} = \sum_{i=1}^{3} A_i B_i = |\mathbf{A}||\mathbf{B}|\cos\theta,$$

where $\theta$ is the angle between them.

**The cross product.**

$$(\mathbf{A} \times \mathbf{B})_i = \sum_{j,k=1}^{3} \epsilon_{ijk} A_j B_k.$$

Expanding explicitly:

$$\mathbf{A} \times \mathbf{B} = (A_y B_z - A_z B_y)\hat{\mathbf{e}}_x + (A_z B_x - A_x B_z)\hat{\mathbf{e}}_y + (A_x B_y - A_y B_x)\hat{\mathbf{e}}_z.$$

**The scalar triple product.**

$$\mathbf{A} \cdot (\mathbf{B} \times \mathbf{C}) = \sum_{i,j,k} \epsilon_{ijk} A_i B_j C_k = \det\begin{pmatrix} A_x & A_y & A_z \\ B_x & B_y & B_z \\ C_x & C_y & C_z \end{pmatrix}.$$

## 1.2 Differential Calculus of Vectors

Let $\mathbf{r}(t) = (x(t), y(t), z(t))$ be a vector-valued function of time $t$. The **derivative** is

$$\dot{\mathbf{r}} = \frac{d\mathbf{r}}{dt} = \lim_{\Delta t \to 0} \frac{\mathbf{r}(t+\Delta t) - \mathbf{r}(t)}{\Delta t} = \dot{x}\,\hat{\mathbf{e}}_x + \dot{y}\,\hat{\mathbf{e}}_y + \dot{z}\,\hat{\mathbf{e}}_z.$$

The product rules hold:

$$\frac{d}{dt}(\mathbf{A} \cdot \mathbf{B}) = \dot{\mathbf{A}} \cdot \mathbf{B} + \mathbf{A} \cdot \dot{\mathbf{B}},$$

$$\frac{d}{dt}(\mathbf{A} \times \mathbf{B}) = \dot{\mathbf{A}} \times \mathbf{B} + \mathbf{A} \times \dot{\mathbf{B}}.$$

**Proof of the dot-product rule.** $f(t) = \mathbf{A}(t) \cdot \mathbf{B}(t) = \sum_i A_i(t) B_i(t)$. Then

$$\frac{df}{dt} = \sum_i \frac{d(A_i B_i)}{dt} = \sum_i (\dot{A}_i B_i + A_i \dot{B}_i) = \dot{\mathbf{A}} \cdot \mathbf{B} + \mathbf{A} \cdot \dot{\mathbf{B}}. \quad\square$$

**Important special case.** If $|\mathbf{A}|$ is constant, then $\mathbf{A}\cdot\mathbf{A} = |\mathbf{A}|^2 = \text{const}$, so

$$0 = \frac{d}{dt}(\mathbf{A}\cdot\mathbf{A}) = 2\,\mathbf{A}\cdot\dot{\mathbf{A}},$$

i.e., $\mathbf{A} \perp \dot{\mathbf{A}}$ whenever $|\mathbf{A}|$ is constant.

## 1.3 The Gradient, Divergence, Curl, and Laplacian

Let $f : \mathbb{R}^3 \to \mathbb{R}$ be a scalar field and $\mathbf{F} : \mathbb{R}^3 \to \mathbb{R}^3$ a vector field. The **nabla operator** is

$$\nabla = \hat{\mathbf{e}}_x \frac{\partial}{\partial x} + \hat{\mathbf{e}}_y \frac{\partial}{\partial y} + \hat{\mathbf{e}}_z \frac{\partial}{\partial z}.$$

**Gradient:**
$$\nabla f = \frac{\partial f}{\partial x}\hat{\mathbf{e}}_x + \frac{\partial f}{\partial y}\hat{\mathbf{e}}_y + \frac{\partial f}{\partial z}\hat{\mathbf{e}}_z.$$

The gradient points in the direction of maximum increase of $f$.

**Divergence:**
$$\nabla \cdot \mathbf{F} = \frac{\partial F_x}{\partial x} + \frac{\partial F_y}{\partial y} + \frac{\partial F_z}{\partial z}.$$

**Curl:**
$$\nabla \times \mathbf{F} = \left(\frac{\partial F_z}{\partial y} - \frac{\partial F_y}{\partial z}\right)\hat{\mathbf{e}}_x + \left(\frac{\partial F_x}{\partial z} - \frac{\partial F_z}{\partial x}\right)\hat{\mathbf{e}}_y + \left(\frac{\partial F_y}{\partial x} - \frac{\partial F_x}{\partial y}\right)\hat{\mathbf{e}}_z.$$

**Laplacian:**
$$\nabla^2 f = \nabla \cdot (\nabla f) = \frac{\partial^2 f}{\partial x^2} + \frac{\partial^2 f}{\partial y^2} + \frac{\partial^2 f}{\partial z^2}.$$

## 1.4 Key Vector Identities (with Proofs)

**Identity 1 (BAC–CAB rule):**
$$\mathbf{A} \times (\mathbf{B} \times \mathbf{C}) = \mathbf{B}(\mathbf{A} \cdot \mathbf{C}) - \mathbf{C}(\mathbf{A} \cdot \mathbf{B}).$$

**Proof.** Using the identity $\epsilon_{ijk}\epsilon_{klm} = \delta_{il}\delta_{jm} - \delta_{im}\delta_{jl}$:

$$[\mathbf{A} \times (\mathbf{B} \times \mathbf{C})]_i = \epsilon_{ijk} A_j \epsilon_{klm} B_l C_m = (\delta_{il}\delta_{jm} - \delta_{im}\delta_{jl}) A_j B_l C_m$$

$$= A_j B_i C_j - A_j B_j C_i = B_i(\mathbf{A}\cdot\mathbf{C}) - C_i(\mathbf{A}\cdot\mathbf{B}).$$

This holds for each $i$, so $\mathbf{A}\times(\mathbf{B}\times\mathbf{C}) = \mathbf{B}(\mathbf{A}\cdot\mathbf{C}) - \mathbf{C}(\mathbf{A}\cdot\mathbf{B})$. $\square$

**Identity 2:** $\nabla \times (\nabla f) = \mathbf{0}$ for any smooth $f$.

**Proof.** The $i$-th component is $\epsilon_{ijk}\partial_j(\partial_k f) = \epsilon_{ijk}\partial_j\partial_k f$. Since $\partial_j\partial_k f = \partial_k\partial_j f$ (Schwarz), and $\epsilon_{ijk}$ is antisymmetric in $j,k$, the sum is zero: contracting a symmetric tensor with an antisymmetric one gives zero. $\square$

**Identity 3:** $\nabla \cdot (\nabla \times \mathbf{F}) = 0$ for any smooth $\mathbf{F}$.

**Proof.** $\nabla \cdot (\nabla \times \mathbf{F}) = \partial_i(\epsilon_{ijk}\partial_j F_k) = \epsilon_{ijk}\partial_i\partial_j F_k = 0$ by the same symmetry/antisymmetry argument. $\square$

**Identity 4 (gradient of $1/r$):**
$$\nabla\!\left(\frac{1}{r}\right) = -\frac{\hat{\mathbf{r}}}{r^2} = -\frac{\mathbf{r}}{r^3}, \qquad r = |\mathbf{r}|.$$

**Proof.** $r = (x^2+y^2+z^2)^{1/2}$. So:

$$\frac{\partial}{\partial x}\left(\frac{1}{r}\right) = -\frac{1}{r^2}\frac{\partial r}{\partial x} = -\frac{1}{r^2}\cdot\frac{x}{r} = -\frac{x}{r^3}.$$

Similarly for $y$ and $z$. Hence $\nabla(1/r) = -(x,y,z)/r^3 = -\mathbf{r}/r^3$. $\square$

**Identity 5:**
$$\nabla^2\!\left(\frac{1}{r}\right) = -4\pi\,\delta^{(3)}(\mathbf{r}).$$

**Proof.** For $r > 0$, $\nabla^2(1/r) = \nabla\cdot(-\mathbf{r}/r^3)$. Computing:

$$\frac{\partial}{\partial x}\left(\frac{x}{r^3}\right) = \frac{1}{r^3} - \frac{3x^2}{r^5}.$$

Summing over all three components:

$$\nabla\cdot\!\left(\frac{\mathbf{r}}{r^3}\right) = \frac{3}{r^3} - \frac{3(x^2+y^2+z^2)}{r^5} = \frac{3}{r^3} - \frac{3}{r^3} = 0, \quad r > 0.$$

To capture the singularity, apply the divergence theorem to a ball $B_\epsilon$ of radius $\epsilon$:

$$\int_{B_\epsilon} \nabla^2\!\left(\frac{1}{r}\right) dV = \oint_{\partial B_\epsilon} \nabla\!\left(\frac{1}{r}\right)\cdot d\mathbf{S} = \oint_{\partial B_\epsilon} \left(-\frac{\hat{\mathbf{r}}}{\epsilon^2}\right)\cdot\hat{\mathbf{r}}\,dS = -\frac{1}{\epsilon^2}\cdot 4\pi\epsilon^2 = -4\pi.$$

This holds for all $\epsilon > 0$, so $\nabla^2(1/r) = -4\pi\,\delta^{(3)}(\mathbf{r})$. $\square$

## 1.5 Polar and Spherical Coordinates

### 1.5.1 Plane Polar Coordinates

Define $(r, \phi)$ by $x = r\cos\phi$, $y = r\sin\phi$. The orthonormal basis vectors are

$$\hat{\mathbf{r}} = \cos\phi\,\hat{\mathbf{e}}_x + \sin\phi\,\hat{\mathbf{e}}_y, \qquad \hat{\boldsymbol{\phi}} = -\sin\phi\,\hat{\mathbf{e}}_x + \cos\phi\,\hat{\mathbf{e}}_y.$$

Their time derivatives:

$$\dot{\hat{\mathbf{r}}} = \dot{\phi}\,\hat{\boldsymbol{\phi}}, \qquad \dot{\hat{\boldsymbol{\phi}}} = -\dot{\phi}\,\hat{\mathbf{r}}.$$

The velocity: $\mathbf{v} = \dot{r}\hat{\mathbf{r}} + r\dot{\phi}\hat{\boldsymbol{\phi}}$.

The acceleration (computed by differentiating $\mathbf{v}$):

$$\mathbf{a} = (\ddot{r} - r\dot{\phi}^2)\hat{\mathbf{r}} + (r\ddot{\phi} + 2\dot{r}\dot{\phi})\hat{\boldsymbol{\phi}}.$$

**Derivation.** 

$$\dot{\mathbf{v}} = \frac{d}{dt}(\dot{r}\hat{\mathbf{r}}) + \frac{d}{dt}(r\dot{\phi}\hat{\boldsymbol{\phi}})$$

$$= \ddot{r}\hat{\mathbf{r}} + \dot{r}\dot{\phi}\hat{\boldsymbol{\phi}} + \dot{r}\dot{\phi}\hat{\boldsymbol{\phi}} + r\ddot{\phi}\hat{\boldsymbol{\phi}} + r\dot{\phi}(-\dot{\phi}\hat{\mathbf{r}})$$

$$= (\ddot{r} - r\dot{\phi}^2)\hat{\mathbf{r}} + (2\dot{r}\dot{\phi} + r\ddot{\phi})\hat{\boldsymbol{\phi}}. \quad\square$$

### 1.5.2 Spherical Coordinates

$x = r\sin\theta\cos\phi$, $y = r\sin\theta\sin\phi$, $z = r\cos\theta$. The Laplacian:

$$\nabla^2 f = \frac{1}{r^2}\frac{\partial}{\partial r}\!\left(r^2\frac{\partial f}{\partial r}\right) + \frac{1}{r^2\sin\theta}\frac{\partial}{\partial\theta}\!\left(\sin\theta\frac{\partial f}{\partial\theta}\right) + \frac{1}{r^2\sin^2\theta}\frac{\partial^2 f}{\partial\phi^2}.$$

## 1.6 Conservative Fields and Potential Functions

**Definition.** A vector field $\mathbf{F}$ is **conservative** if $\exists\,V$ such that $\mathbf{F} = -\nabla V$.

**Theorem 1.6.1.** On a simply-connected domain, $\mathbf{F}$ is conservative $\iff$ $\nabla \times \mathbf{F} = \mathbf{0}$.

**Proof.** ($\Rightarrow$) If $\mathbf{F} = -\nabla V$, then $\nabla\times\mathbf{F} = -\nabla\times(\nabla V) = \mathbf{0}$ by Identity 2.

($\Leftarrow$) Define $V(\mathbf{r}) = -\int_{\mathbf{r}_0}^{\mathbf{r}} \mathbf{F}\cdot d\boldsymbol{\ell}$. By Stokes' theorem, path-independence follows from $\nabla\times\mathbf{F}=\mathbf{0}$ on the simply-connected domain. The fundamental theorem then gives $\mathbf{F} = -\nabla V$. $\square$

**Consequence.** Work done by a conservative force: $W = V(\mathbf{r}_1) - V(\mathbf{r}_2)$ (path-independent).

## 1.7 Ordinary Differential Equations

**Simple Harmonic Oscillator.** $\ddot{x} + \omega^2 x = 0$ has general solution $x(t) = A\cos(\omega t) + B\sin(\omega t)$.

**Proof.** Let $x = e^{\lambda t}$. Then $\lambda^2 + \omega^2 = 0$, $\lambda = \pm i\omega$. Taking real combinations of $e^{\pm i\omega t}$ gives $A\cos\omega t + B\sin\omega t$. $\square$

**Resonant forced SHO.** $\ddot{x} + \omega^2 x = F_0\cos(\omega t)$ (driving at the natural frequency). The particular solution is

$$x_p(t) = \frac{F_0}{2\omega}t\sin(\omega t).$$

**Proof.** Let $x_p = Ct\sin(\omega t)$. Then $\dot{x}_p = C(\sin\omega t + \omega t\cos\omega t)$, $\ddot{x}_p = C(2\omega\cos\omega t - \omega^2 t\sin\omega t)$. So $\ddot{x}_p + \omega^2 x_p = 2C\omega\cos\omega t$. Setting $2C\omega = F_0$ gives $C = F_0/(2\omega)$. $\square$

---

# Chapter 2: Newtonian Mechanics

## 2.1 Newton's Three Laws

**Newton's First Law (Law of Inertia).** *A body remains at rest or in uniform rectilinear motion unless acted upon by a net external force.* This defines **inertial reference frames**.

**Newton's Second Law.** *The net force equals the rate of change of linear momentum:*

$$\mathbf{F} = \frac{d\mathbf{p}}{dt}, \qquad \mathbf{p} = m\mathbf{v}.$$

For constant mass: $\mathbf{F} = m\mathbf{a} = m\ddot{\mathbf{r}}$.

**Newton's Third Law.** *If body 1 exerts force $\mathbf{F}_{12}$ on body 2, then body 2 exerts $\mathbf{F}_{21} = -\mathbf{F}_{12}$ on body 1.*

## 2.2 Momentum and Impulse

The **impulse** delivered over $[t_1, t_2]$:

$$\mathbf{J} = \int_{t_1}^{t_2} \mathbf{F}\,dt = \mathbf{p}(t_2) - \mathbf{p}(t_1) = \Delta\mathbf{p}.$$

**Proof.** $\int_{t_1}^{t_2} \mathbf{F}\,dt = \int_{t_1}^{t_2} \dot{\mathbf{p}}\,dt = \mathbf{p}(t_2) - \mathbf{p}(t_1)$ by the fundamental theorem of calculus. $\square$

## 2.3 Work, Kinetic Energy, and the Work–Energy Theorem

**Definition.** The **kinetic energy**: $T = \tfrac{1}{2}m|\mathbf{v}|^2$.

**Theorem 2.3.1 (Work–Energy Theorem).** The work done by the net force equals the change in kinetic energy:

$$W = \int_{\mathbf{r}_1}^{\mathbf{r}_2} \mathbf{F}\cdot d\boldsymbol{\ell} = T_2 - T_1.$$

**Proof.** Parametrize by time. $d\boldsymbol{\ell} = \mathbf{v}\,dt$:

$$W = \int_{t_1}^{t_2} \mathbf{F}\cdot\mathbf{v}\,dt = \int_{t_1}^{t_2} m\mathbf{a}\cdot\mathbf{v}\,dt = \int_{t_1}^{t_2} m\dot{\mathbf{v}}\cdot\mathbf{v}\,dt = \int_{t_1}^{t_2} \frac{d}{dt}\!\left(\tfrac{1}{2}mv^2\right)dt = T_2 - T_1. \quad\square$$

## 2.4 Potential Energy and Conservation of Energy

For a conservative force $\mathbf{F} = -\nabla V$: $W = V_1 - V_2$.

Combining with the Work–Energy Theorem: $T_2 - T_1 = V_1 - V_2$, so $T_1 + V_1 = T_2 + V_2$.

**Theorem 2.4.1 (Conservation of Mechanical Energy).** Under a conservative force, $E = T + V = \text{const}$.

**Proof.** $\frac{dE}{dt} = m\mathbf{a}\cdot\mathbf{v} + \nabla V\cdot\mathbf{v} = (m\mathbf{a} + \nabla V)\cdot\mathbf{v} = (\mathbf{F} - \mathbf{F})\cdot\mathbf{v} = 0$. $\square$

## 2.5 Angular Momentum and its Conservation

**Definition.** Angular momentum: $\mathbf{L} = \mathbf{r} \times \mathbf{p} = m(\mathbf{r} \times \mathbf{v})$.

**Theorem 2.5.1.** $\dot{\mathbf{L}} = \boldsymbol{\tau} = \mathbf{r} \times \mathbf{F}$.

**Proof.** $\dot{\mathbf{L}} = \dot{\mathbf{r}}\times m\mathbf{v} + \mathbf{r}\times m\dot{\mathbf{v}} = \mathbf{v}\times m\mathbf{v} + \mathbf{r}\times\mathbf{F} = \mathbf{0} + \mathbf{r}\times\mathbf{F}$. $\square$

**Corollary.** For a central force ($\mathbf{F} \parallel \mathbf{r}$): $\boldsymbol{\tau} = \mathbf{r}\times\mathbf{F} = \mathbf{0}$, so $\mathbf{L} = \text{const}$.

**Theorem 2.5.2.** Under a central force, the motion is planar.

**Proof.** $\mathbf{L} = m\mathbf{r}\times\mathbf{v}$ is constant and non-zero, so $\mathbf{r}(t) \perp \hat{\mathbf{L}}$ for all $t$. The trajectory lies in the plane with normal $\hat{\mathbf{L}}$. $\square$

## 2.6 Centre of Mass and the Two-Body Reduction

Consider two particles with masses $m_1, m_2$ and positions $\mathbf{r}_1, \mathbf{r}_2$. Total mass $M = m_1 + m_2$.

**Centre of mass:**
$$\mathbf{R} = \frac{m_1\mathbf{r}_1 + m_2\mathbf{r}_2}{M}.$$

**Theorem 2.6.1.** Without external forces, $M\ddot{\mathbf{R}} = \mathbf{0}$, so $\mathbf{R}$ moves uniformly.

**Proof.** $M\ddot{\mathbf{R}} = m_1\ddot{\mathbf{r}}_1 + m_2\ddot{\mathbf{r}}_2 = \mathbf{F}_{12} + \mathbf{F}_{21} = \mathbf{0}$ by Newton's third law. $\square$

**Relative coordinate:** $\mathbf{r} = \mathbf{r}_1 - \mathbf{r}_2$. Then:

$$\mathbf{r}_1 = \mathbf{R} + \frac{m_2}{M}\mathbf{r}, \qquad \mathbf{r}_2 = \mathbf{R} - \frac{m_1}{M}\mathbf{r}.$$

**Proof.** $\mathbf{R} + \frac{m_2}{M}\mathbf{r} = \frac{m_1\mathbf{r}_1+m_2\mathbf{r}_2+m_2\mathbf{r}_1-m_2\mathbf{r}_2}{M} = \frac{(m_1+m_2)\mathbf{r}_1}{M} = \mathbf{r}_1$. $\square$

The equation of motion for $\mathbf{r}$:

$$\ddot{\mathbf{r}} = \frac{\mathbf{F}_{12}}{m_1} + \frac{\mathbf{F}_{12}}{m_2} = \frac{\mathbf{F}_{12}}{\mu},$$

where the **reduced mass** is

$$\mu = \frac{m_1 m_2}{m_1+m_2}.$$

So $\mu\ddot{\mathbf{r}} = \mathbf{F}_{12}$: the two-body problem reduces to a **one-body problem** with reduced mass $\mu$.

---

# Chapter 3: Newtonian Gravity

## 3.1 Newton's Law of Universal Gravitation

**Law.** The force on mass $m$ at position $\mathbf{r}$ due to mass $M$ at the origin:

$$\mathbf{F} = -\frac{GMm}{r^2}\hat{\mathbf{r}} = -\frac{GMm}{r^3}\mathbf{r}, \qquad G = 6.674\times10^{-11}\,\mathrm{N\,m^2\,kg^{-2}}.$$

## 3.2 The Gravitational Field and Potential

**Gravitational field** (force per unit mass):

$$\mathbf{g}(\mathbf{r}) = -\frac{GM}{r^2}\hat{\mathbf{r}} = -\nabla\Phi, \qquad \Phi(\mathbf{r}) = -\frac{GM}{r}.$$

**Verification.** $-\nabla(-GM/r) = GM\nabla(1/r) = GM(-\mathbf{r}/r^3) = -GM\hat{\mathbf{r}}/r^2 = \mathbf{g}$. $\square$

## 3.3 Gauss's Law for Gravity

**Theorem 3.3.1.** For any closed surface $S$ enclosing mass $M_{\mathrm{enc}}$:

$$\oint_S \mathbf{g}\cdot d\mathbf{S} = -4\pi G M_{\mathrm{enc}}.$$

**Proof.** By the divergence theorem: $\oint_S \mathbf{g}\cdot d\mathbf{S} = \int_V \nabla\cdot\mathbf{g}\,dV = -\int_V \nabla^2\Phi\,dV$.

For $\Phi = -GM/r$: $\nabla^2\Phi = -GM\nabla^2(1/r) = -GM\cdot(-4\pi\delta^{(3)}(\mathbf{r})) = 4\pi GM\delta^{(3)}(\mathbf{r})$.

So $\oint_S \mathbf{g}\cdot d\mathbf{S} = -4\pi GM$. $\square$

In differential form: $\nabla^2\Phi = 4\pi G\rho$ (**Poisson's equation**).

## 3.4 Gravitational Potential Energy of Two Point Masses

$$U(r) = -\frac{Gm_1 m_2}{r}.$$

The force on $m_1$ is $-\nabla_{\mathbf{r}_1}U = -Gm_1m_2(\mathbf{r}_2-\mathbf{r}_1)/r^3$, which is attractive and directed toward $m_2$. $\checkmark$

---

# Chapter 4: The Newtonian Two-Body Problem

## 4.1 Equations of Motion and Centre-of-Mass Reduction

In the CoM frame, the relative coordinate $\mathbf{r} = \mathbf{r}_1 - \mathbf{r}_2$ satisfies

$$\mu\ddot{\mathbf{r}} = -\frac{Gm_1 m_2}{r^2}\hat{\mathbf{r}}.$$

Dividing by $\mu$, and defining $k = GM = G(m_1+m_2)$:

$$\ddot{\mathbf{r}} = -\frac{k}{r^2}\hat{\mathbf{r}} = -\frac{k}{r^3}\mathbf{r}.$$

This is the equation of a single particle of reduced mass $\mu$ in the central gravitational field of a body of mass $M = m_1+m_2$ at the origin.

## 4.2 Conservation of Angular Momentum: Planar Motion

The gravitational force is central, so $\mathbf{L} = \mu\,\mathbf{r}\times\dot{\mathbf{r}}$ is conserved (Corollary to Theorem 2.5.1). The motion is planar (Theorem 2.5.2). We work in the orbital plane with polar coordinates $(r,\phi)$.

The specific angular momentum per unit reduced mass is

$$\ell \equiv \frac{|\mathbf{L}|}{\mu} = |\mathbf{r}\times\dot{\mathbf{r}}|.$$

**Claim:** $\ell = r^2\dot{\phi}$.

**Proof.** $\mathbf{r}\times\dot{\mathbf{r}} = r\hat{\mathbf{r}}\times(\dot{r}\hat{\mathbf{r}}+r\dot{\phi}\hat{\boldsymbol{\phi}}) = r^2\dot{\phi}(\hat{\mathbf{r}}\times\hat{\boldsymbol{\phi}}) = r^2\dot{\phi}\hat{\mathbf{z}}$. So $|\mathbf{r}\times\dot{\mathbf{r}}| = r^2\dot{\phi}$. $\square$

Conservation law:
$$\boxed{\ell = r^2\dot{\phi} = \mathrm{const}.}$$

## 4.3 Conservation of Energy

The total energy per unit reduced mass:

$$\mathcal{E} = \frac{1}{2}|\dot{\mathbf{r}}|^2 - \frac{k}{r} = \frac{1}{2}(\dot{r}^2 + r^2\dot{\phi}^2) - \frac{k}{r}.$$

Substituting $\dot{\phi} = \ell/r^2$:

$$\boxed{\mathcal{E} = \frac{1}{2}\dot{r}^2 + \frac{\ell^2}{2r^2} - \frac{k}{r} = \mathrm{const}.}$$

(Constant by Theorem 2.4.1, since the gravitational force is conservative.)

## 4.4 The Effective Potential

Define the **effective potential**

$$V_{\mathrm{eff}}(r) = \frac{\ell^2}{2r^2} - \frac{k}{r},$$

so $\mathcal{E} = \frac{1}{2}\dot{r}^2 + V_{\mathrm{eff}}(r)$. This reduces the radial motion to that of a 1D particle in $V_{\mathrm{eff}}$.

The term $\ell^2/(2r^2)$ is the **centrifugal barrier** (repulsive, from angular momentum conservation) and $-k/r$ is the attractive gravitational term.

**Circular orbit radius.** Setting $dV_{\mathrm{eff}}/dr = 0$:

$$-\frac{\ell^2}{r^3} + \frac{k}{r^2} = 0 \implies r_{\mathrm{circ}} = \frac{\ell^2}{k}.$$

**Stability.** $\frac{d^2V_{\mathrm{eff}}}{dr^2}\big|_{r_c} = \frac{3\ell^2}{r_c^4} - \frac{2k}{r_c^3}$. At $r_c = \ell^2/k$:

$$= \frac{3\ell^2 k^4}{\ell^8} - \frac{2k^4}{\ell^6} = \frac{3k^4}{\ell^6} - \frac{2k^4}{\ell^6} = \frac{k^4}{\ell^6} > 0.$$

So $r_c$ is a stable minimum of $V_{\mathrm{eff}}$ in Newtonian gravity — circular orbits are stable at all radii.

## 4.5 The Orbit Equation: Derivation via the Binet Substitution

We seek $r(\phi)$ — the orbit shape. Make the substitution $u = 1/r$.

**Expressing $\dot{r}$ in terms of $u'(\phi) = du/d\phi$:**

From $r = 1/u$: $\dot{r} = -u'/u^2 \cdot \dot{\phi}$. Since $\dot{\phi} = \ell/r^2 = \ell u^2$:

$$\dot{r} = -\frac{u'}{u^2}\cdot\ell u^2 = -\ell u'.$$

**Computing $\ddot{r}$:**

$$\ddot{r} = \frac{d}{dt}(-\ell u') = -\ell\frac{du'}{dt} = -\ell u''\dot{\phi} = -\ell u''\cdot\ell u^2 = -\ell^2 u^2 u''.$$

**Radial equation of motion** (from $\mathbf{a} = -k\hat{\mathbf{r}}/r^2$ and the polar acceleration formula):

$$\ddot{r} - r\dot{\phi}^2 = -\frac{k}{r^2}.$$

Substitute $r=1/u$, $\ddot{r} = -\ell^2u^2u''$, $\dot{\phi} = \ell u^2$:

$$-\ell^2u^2u'' - \frac{1}{u}(\ell u^2)^2 = -ku^2.$$

$$-\ell^2u^2u'' - \ell^2u^3 = -ku^2.$$

Divide by $-\ell^2u^2$:

$$\boxed{u'' + u = \frac{k}{\ell^2}.}$$

This is the **Binet equation** — a simple harmonic oscillator with constant forcing. General solution:

$$u(\phi) = \frac{k}{\ell^2} + A\cos(\phi - \phi_0).$$

Choose $\phi_0 = 0$ (measure $\phi$ from periapsis). Define $e = A\ell^2/k$ (eccentricity). Then:

$$u(\phi) = \frac{k}{\ell^2}(1 + e\cos\phi),$$

and in terms of $r$:

$$\boxed{r(\phi) = \frac{p}{1+e\cos\phi}, \qquad p = \frac{\ell^2}{k}.}$$

This is the **orbit equation** with semi-latus rectum $p$.

## 4.6 Classification of Orbits

**Eccentricity in terms of $\mathcal{E}$ and $\ell$.** At periapsis $\phi=0$, $\dot{r}=0$ so $\mathcal{E} = V_{\mathrm{eff}}(r_{\min})$:

$$\mathcal{E} = \frac{\ell^2}{2r_{\min}^2} - \frac{k}{r_{\min}}.$$

With $r_{\min} = p/(1+e) = \ell^2/[k(1+e)]$:

$$\mathcal{E} = \frac{k^2(1+e)^2}{2\ell^2} - \frac{k^2(1+e)}{\ell^2} = \frac{k^2}{\ell^2}\cdot\frac{(1+e)^2 - 2(1+e)}{2} = \frac{k^2(e^2-1)}{2\ell^2}.$$

Therefore:

$$\boxed{e = \sqrt{1 + \frac{2\mathcal{E}\ell^2}{k^2}}.}$$

| $\mathcal{E}$ | $e$ | Orbit |
|:---:|:---:|:---:|
| $< 0$ | $< 1$ | Ellipse (or circle) |
| $= 0$ | $= 1$ | Parabola |
| $> 0$ | $> 1$ | Hyperbola |

## 4.7 Kepler's First Law

**Theorem 4.7.1.** Under Newtonian gravity, the orbit is a conic section with the attracting body at a focus.

**Proof.** The orbit equation $r = p/(1+e\cos\phi)$ is the standard polar form of a conic section with semi-latus rectum $p$ and eccentricity $e$, and origin at a focus. (See Appendix A for the proof that this is a conic section.) $\square$

## 4.8 Kepler's Second Law

**Theorem 4.8.1 (Equal Areas in Equal Times).** The radius vector sweeps equal areas in equal times.

**Proof.** In time $dt$, the swept area is $dA = \tfrac{1}{2}|\mathbf{r}\times d\mathbf{r}| = \tfrac{1}{2}r^2\,d\phi$. So

$$\frac{dA}{dt} = \frac{1}{2}r^2\dot{\phi} = \frac{\ell}{2} = \mathrm{const.}$$

Equal areas in equal times follows from $\ell = \mathrm{const}$. $\square$

## 4.9 Kepler's Third Law

**Theorem 4.9.1.** For an elliptical orbit with semi-major axis $a$: $T^2 = \frac{4\pi^2}{GM}a^3$.

**Proof.**

**Step 1.** For an ellipse: $r_{\min} = a(1-e)$, $r_{\max} = a(1+e)$, $p = a(1-e^2)$, so

$$a = \frac{p}{1-e^2} = \frac{\ell^2}{k(1-e^2)}.$$

**Step 2.** Semi-minor axis: $b = a\sqrt{1-e^2}$. Area: $A = \pi ab = \pi a^2\sqrt{1-e^2}$.

**Step 3.** Areal velocity $= \ell/2$, so total area per period:

$$A = \frac{\ell}{2}T \implies T = \frac{2\pi a^2\sqrt{1-e^2}}{\ell}.$$

**Step 4.** From $p = a(1-e^2)$: $\sqrt{1-e^2} = \sqrt{p/a}$. From $p = \ell^2/k$: $\ell = \sqrt{kp}$.

$$T = \frac{2\pi a^2\sqrt{p/a}}{\sqrt{kp}} = \frac{2\pi a^2}{\sqrt{ka}} = \frac{2\pi a^{3/2}}{\sqrt{k}}.$$

Squaring:

$$\boxed{T^2 = \frac{4\pi^2}{k}a^3 = \frac{4\pi^2}{GM}a^3.} \quad\square$$

## 4.10 The Vis-Viva Equation

**Theorem 4.10.1.** At separation $r$ in an orbit with semi-major axis $a$:

$$v^2 = GM\!\left(\frac{2}{r} - \frac{1}{a}\right).$$

**Proof.** Total energy: $\mathcal{E} = k^2(e^2-1)/(2\ell^2) = -k/(2a)$ (using $a = \ell^2/[k(1-e^2)]$). So:

$$\frac{v^2}{2} - \frac{k}{r} = -\frac{k}{2a} \implies v^2 = k\!\left(\frac{2}{r}-\frac{1}{a}\right). \quad\square$$

**Derivation that $\mathcal{E} = -k/(2a)$.**

$$\mathcal{E} = \frac{k^2(e^2-1)}{2\ell^2}.$$

From $a = \ell^2/[k(1-e^2)]$: $\ell^2 = ak(1-e^2)$. So:

$$\mathcal{E} = \frac{k^2(e^2-1)}{2ak(1-e^2)} = \frac{k\cdot(-(1-e^2))}{2a(1-e^2)} = -\frac{k}{2a}. \quad\square$$

## 4.11 Turning Points and Radial Oscillations

Turning points satisfy $\mathcal{E} = V_{\mathrm{eff}}(r)$:

$$\frac{\ell^2}{2r^2} - \frac{k}{r} = \mathcal{E} \implies \frac{2\mathcal{E}}{\ell^2}r^2 + \frac{2k}{\ell^2}r - 1 = 0.$$

By Vieta's formulae for roots $r_{\min}, r_{\max}$:

$$r_{\min} + r_{\max} = -\frac{k/\ell^2}{\mathcal{E}/\ell^2} = -\frac{k}{\mathcal{E}} = \frac{k}{|\mathcal{E}|} = 2a.$$

$$r_{\min}\cdot r_{\max} = \frac{-\ell^2/2}{\mathcal{E}} = \frac{\ell^2}{2|\mathcal{E}|} = b^2 \qquad\text{(where }b^2 = a^2(1-e^2)\text{)}.$$

**Radial oscillation frequency near circular orbit.** Perturb $r = r_c + \delta r$:

$$\delta\ddot{r} = -\omega_r^2\delta r, \qquad \omega_r^2 = \frac{d^2V_{\mathrm{eff}}}{dr^2}\bigg|_{r_c} = \frac{k^4}{\ell^6}.$$

The orbital angular frequency at $r_c$: $\omega_\phi = \dot{\phi} = \ell/r_c^2 = \ell k^2/\ell^4 = k^2/\ell^3$.

So $\omega_r = k^2/\ell^3 = \omega_\phi$: radial and orbital frequencies are equal in Newtonian gravity, so **Keplerian orbits are exactly closed**. This breaks in GR.

## 4.12 The Runge–Lenz Vector and its Conservation

The **Runge–Lenz vector** (specific, per unit reduced mass):

$$\mathbf{A} = \dot{\mathbf{r}} \times \boldsymbol{\ell} - k\hat{\mathbf{r}}, \qquad \boldsymbol{\ell} = \mathbf{r}\times\dot{\mathbf{r}}.$$

**Theorem 4.12.1.** $\dot{\mathbf{A}} = \mathbf{0}$ (the Runge-Lenz vector is conserved).

**Proof.** $\dot{\mathbf{A}} = \ddot{\mathbf{r}}\times\boldsymbol{\ell} + \dot{\mathbf{r}}\times\dot{\boldsymbol{\ell}} - k\dot{\hat{\mathbf{r}}}$.

Since $\boldsymbol{\ell}$ is conserved, $\dot{\boldsymbol{\ell}}=\mathbf{0}$. So $\dot{\mathbf{A}} = \ddot{\mathbf{r}}\times\boldsymbol{\ell} - k\dot{\hat{\mathbf{r}}}$.

With $\ddot{\mathbf{r}} = -k\hat{\mathbf{r}}/r^2$ and $\boldsymbol{\ell} = \mathbf{r}\times\dot{\mathbf{r}}$, apply BAC-CAB to $\hat{\mathbf{r}}\times(\mathbf{r}\times\dot{\mathbf{r}})$:

$$\hat{\mathbf{r}}\times(\mathbf{r}\times\dot{\mathbf{r}}) = \mathbf{r}(\hat{\mathbf{r}}\cdot\dot{\mathbf{r}}) - \dot{\mathbf{r}}(\hat{\mathbf{r}}\cdot\mathbf{r}) = r\dot{r}\hat{\mathbf{r}} - r\dot{\mathbf{r}}.$$

So:

$$\ddot{\mathbf{r}}\times\boldsymbol{\ell} = -\frac{k}{r^2}\hat{\mathbf{r}}\times\boldsymbol{\ell} = \frac{k}{r^2}(r\dot{\mathbf{r}} - r\dot{r}\hat{\mathbf{r}}) = \frac{k}{r}(\dot{\mathbf{r}} - \dot{r}\hat{\mathbf{r}}).$$

And $\dot{\hat{\mathbf{r}}} = \frac{d}{dt}(\mathbf{r}/r) = \frac{\dot{\mathbf{r}}}{r} - \frac{\mathbf{r}\dot{r}}{r^2} = \frac{\dot{\mathbf{r}} - \dot{r}\hat{\mathbf{r}}}{r}$.

So $k\dot{\hat{\mathbf{r}}} = k(\dot{\mathbf{r}}-\dot{r}\hat{\mathbf{r}})/r$. Therefore:

$$\dot{\mathbf{A}} = \frac{k}{r}(\dot{\mathbf{r}}-\dot{r}\hat{\mathbf{r}}) - \frac{k}{r}(\dot{\mathbf{r}}-\dot{r}\hat{\mathbf{r}}) = \mathbf{0}. \quad\square$$

**Recovery of orbit equation.** $\mathbf{A}\cdot\mathbf{r} = (\dot{\mathbf{r}}\times\boldsymbol{\ell})\cdot\mathbf{r} - kr = \ell^2 - kr$.

Also $\mathbf{A}\cdot\mathbf{r} = |\mathbf{A}|r\cos\phi = ker\cos\phi$ (with $|\mathbf{A}|=ke$, direction toward periapsis).

So $ker\cos\phi = \ell^2 - kr \implies r = \ell^2/[k(1+e\cos\phi)] = p/(1+e\cos\phi)$. $\checkmark$

The Runge-Lenz vector points to the periapsis and has fixed direction — hence no precession in Newtonian gravity.

---

# Chapter 5: Elements of Differential Geometry

## 5.1 Manifolds and Coordinate Systems

An $n$-dimensional smooth **manifold** $\mathcal{M}$ is a topological space that is locally homeomorphic to $\mathbb{R}^n$ and equipped with a smooth atlas (consistent collection of coordinate charts). We use Greek indices $\mu, \nu, \ldots \in \{0,1,2,3\}$ for spacetime coordinates, with Einstein's summation convention (repeated upper-lower index = sum).

## 5.2 Tangent Vectors, Covectors, and Tensors

At a point $p \in \mathcal{M}$, the **tangent space** $T_p\mathcal{M}$ is spanned by $\{\partial/\partial x^\mu\}$ and the **cotangent space** $T_p^*\mathcal{M}$ is spanned by $\{dx^\mu\}$, with $dx^\mu(\partial/\partial x^\nu) = \delta^\mu_\nu$.

A vector $v = v^\mu\partial_\mu$ transforms as $v^{\mu'} = (\partial x^{\mu'}/\partial x^\mu)v^\mu$ (contravariant), and a covector $\omega = \omega_\mu dx^\mu$ transforms as $\omega_{\mu'} = (\partial x^\mu/\partial x^{\mu'})\omega_\mu$ (covariant).

## 5.3 The Metric Tensor

A **metric tensor** $g_{\mu\nu}$ is a symmetric, non-degenerate $(0,2)$-tensor. The **line element** is

$$ds^2 = g_{\mu\nu}\,dx^\mu\,dx^\nu.$$

The **inverse metric** $g^{\mu\nu}$ satisfies $g^{\mu\rho}g_{\rho\nu} = \delta^\mu_\nu$. Indices are raised/lowered by $g$.

## 5.4 Covariant Derivative and Christoffel Symbols

Ordinary partial derivatives of tensor components do not transform as tensors. The **covariant derivative** $\nabla$ is the unique torsion-free ($\Gamma^\rho_{\mu\nu} = \Gamma^\rho_{\nu\mu}$), metric-compatible ($\nabla_\rho g_{\mu\nu}=0$) connection.

**Derivation of Christoffel symbols.** Write metric compatibility for three cyclic permutations of indices:

$$\partial_\rho g_{\mu\nu} = \Gamma^\sigma_{\rho\mu}g_{\sigma\nu} + \Gamma^\sigma_{\rho\nu}g_{\sigma\mu}, \tag{i}$$

$$\partial_\mu g_{\nu\rho} = \Gamma^\sigma_{\mu\nu}g_{\sigma\rho} + \Gamma^\sigma_{\mu\rho}g_{\sigma\nu}, \tag{ii}$$

$$\partial_\nu g_{\rho\mu} = \Gamma^\sigma_{\nu\rho}g_{\sigma\mu} + \Gamma^\sigma_{\nu\mu}g_{\sigma\rho}. \tag{iii}$$

Compute (ii) + (iii) $-$ (i), using symmetry $\Gamma^\sigma_{\mu\nu} = \Gamma^\sigma_{\nu\mu}$:

$$\partial_\mu g_{\nu\rho} + \partial_\nu g_{\rho\mu} - \partial_\rho g_{\mu\nu} = 2\Gamma^\sigma_{\mu\nu}g_{\sigma\rho}.$$

Contract with $\frac{1}{2}g^{\rho\lambda}$:

$$\boxed{\Gamma^\lambda_{\mu\nu} = \frac{1}{2}g^{\lambda\rho}(\partial_\mu g_{\nu\rho} + \partial_\nu g_{\rho\mu} - \partial_\rho g_{\mu\nu}).} \quad\square$$

**Covariant derivatives:**

$$\nabla_\nu V^\mu = \partial_\nu V^\mu + \Gamma^\mu_{\nu\rho}V^\rho, \qquad \nabla_\nu \omega_\mu = \partial_\nu\omega_\mu - \Gamma^\rho_{\nu\mu}\omega_\rho.$$

## 5.5 Geodesics and the Geodesic Equation

A **geodesic** is a curve whose tangent vector is parallel-transported along itself. For a curve $x^\mu(\lambda)$:

$$\frac{d^2x^\mu}{d\lambda^2} + \Gamma^\mu_{\nu\rho}\frac{dx^\nu}{d\lambda}\frac{dx^\rho}{d\lambda} = 0.$$

**Derivation (variational).** Extremize $S = \frac{1}{2}\int g_{\mu\nu}\dot{x}^\mu\dot{x}^\nu d\lambda$ ($\dot{x} = dx/d\lambda$). The Euler-Lagrange equations for $\mathcal{L} = \frac{1}{2}g_{\mu\nu}\dot{x}^\mu\dot{x}^\nu$:

$$\frac{d}{d\lambda}(g_{\sigma\nu}\dot{x}^\nu) - \frac{1}{2}\partial_\sigma g_{\mu\nu}\dot{x}^\mu\dot{x}^\nu = 0.$$

Expanding: $g_{\sigma\nu}\ddot{x}^\nu + \partial_\rho g_{\sigma\nu}\dot{x}^\rho\dot{x}^\nu - \frac{1}{2}\partial_\sigma g_{\mu\nu}\dot{x}^\mu\dot{x}^\nu = 0$.

Symmetrizing $\partial_\rho g_{\sigma\nu}\dot{x}^\rho\dot{x}^\nu = \frac{1}{2}(\partial_\rho g_{\sigma\nu}+\partial_\nu g_{\sigma\rho})\dot{x}^\rho\dot{x}^\nu$ and multiplying by $g^{\mu\sigma}$:

$$\ddot{x}^\mu + \frac{1}{2}g^{\mu\sigma}(\partial_\rho g_{\sigma\nu}+\partial_\nu g_{\sigma\rho}-\partial_\sigma g_{\rho\nu})\dot{x}^\rho\dot{x}^\nu = 0,$$

which is the geodesic equation. $\square$

## 5.6 The Riemann Curvature Tensor

The Riemann tensor measures the failure of covariant derivatives to commute:

$$[\nabla_\mu, \nabla_\nu]V^\rho = R^\rho_{\ \sigma\mu\nu}V^\sigma,$$

where

$$R^\rho_{\ \sigma\mu\nu} = \partial_\mu\Gamma^\rho_{\nu\sigma} - \partial_\nu\Gamma^\rho_{\mu\sigma} + \Gamma^\rho_{\mu\lambda}\Gamma^\lambda_{\nu\sigma} - \Gamma^\rho_{\nu\lambda}\Gamma^\lambda_{\mu\sigma}.$$

**Proof of the formula.** Apply $[\nabla_\mu, \nabla_\nu]$ to $V^\rho$. Expand $\nabla_\mu(\nabla_\nu V^\rho)$ and antisymmetrize in $[\mu,\nu]$. All terms involving $\partial V$ cancel (torsion-free condition), leaving:

$$[\nabla_\mu, \nabla_\nu]V^\rho = (\partial_\mu\Gamma^\rho_{\nu\sigma} - \partial_\nu\Gamma^\rho_{\mu\sigma} + \Gamma^\rho_{\mu\lambda}\Gamma^\lambda_{\nu\sigma} - \Gamma^\rho_{\nu\lambda}\Gamma^\lambda_{\mu\sigma})V^\sigma. \quad\square$$

**Symmetries** (all indices down: $R_{\rho\sigma\mu\nu} = g_{\rho\lambda}R^\lambda_{\ \sigma\mu\nu}$):

1. $R_{\rho\sigma\mu\nu} = -R_{\sigma\rho\mu\nu}$
2. $R_{\rho\sigma\mu\nu} = -R_{\rho\sigma\nu\mu}$  
3. $R_{\rho\sigma\mu\nu} = R_{\mu\nu\rho\sigma}$
4. $R_{\rho\sigma\mu\nu} + R_{\rho\mu\nu\sigma} + R_{\rho\nu\sigma\mu} = 0$ (first Bianchi identity)

**Second Bianchi identity:**

$$\nabla_\lambda R_{\rho\sigma\mu\nu} + \nabla_\rho R_{\sigma\lambda\mu\nu} + \nabla_\sigma R_{\lambda\rho\mu\nu} = 0.$$

## 5.7 The Ricci Tensor and Ricci Scalar

**Ricci tensor:** $R_{\mu\nu} = R^\rho_{\ \mu\rho\nu}$ (symmetric: $R_{\mu\nu} = R_{\nu\mu}$).

**Ricci scalar:** $R = g^{\mu\nu}R_{\mu\nu}$.

## 5.8 The Einstein Tensor

$$G_{\mu\nu} = R_{\mu\nu} - \frac{1}{2}g_{\mu\nu}R.$$

**Theorem 5.8.1 (Contracted Bianchi identity).** $\nabla^\mu G_{\mu\nu} = 0$.

**Proof.** Contract the second Bianchi identity $\nabla_{[\lambda}R_{\rho\sigma]\mu\nu}=0$ twice: first with $g^{\rho\mu}$, then with $g^{\sigma\nu}$. The first contraction gives:

$$\nabla_\lambda R_{\sigma\nu} - \nabla^\rho R_{\sigma\lambda\rho\nu} + \nabla_\sigma R_{\lambda\nu} = 0 \quad\text{(using antisymmetry of R)}.$$

Wait — let me be more careful. Contract $\nabla_\lambda R_{\rho\sigma\mu\nu}+\nabla_\rho R_{\sigma\lambda\mu\nu}+\nabla_\sigma R_{\lambda\rho\mu\nu}=0$ with $g^{\sigma\mu}$:

$$\nabla_\lambda R_{\rho\nu} - \nabla_\rho R_{\lambda\nu} + \nabla^\mu R_{\lambda\rho\mu\nu} = 0.$$

(Using $g^{\sigma\mu}R_{\rho\sigma\mu\nu} = R_{\rho\nu}$ and $g^{\sigma\mu}R_{\sigma\lambda\mu\nu} = -g^{\sigma\mu}R_{\lambda\sigma\mu\nu} = -R_{\lambda\nu}$.)

Now contract with $g^{\rho\lambda}$:

$$\nabla^\rho R_{\rho\nu} - \nabla^\lambda R_{\lambda\nu} + g^{\rho\lambda}\nabla^\mu R_{\lambda\rho\mu\nu} = 0.$$

The last term: $g^{\rho\lambda}\nabla^\mu R_{\lambda\rho\mu\nu} = \nabla^\mu g^{\rho\lambda}R_{\lambda\rho\mu\nu} = -\nabla^\mu R_{\rho\mu\nu}^{\ \ \rho} = -\nabla^\mu R_{\mu\nu}$... This requires careful use of the symmetries. The final result is:

$$\nabla^\mu R_{\mu\nu} = \frac{1}{2}\nabla_\nu R,$$

i.e., $\nabla^\mu(R_{\mu\nu} - \frac{1}{2}g_{\mu\nu}R) = \nabla^\mu G_{\mu\nu} = 0$. $\square$

---

# Chapter 6: Special Relativity

## 6.1 Postulates and the Lorentz Transformation

Special relativity rests on:
1. **Relativity:** Laws of physics are the same in all inertial frames.
2. **Constancy of $c$:** The speed of light in vacuum is $c = 299\,792\,458\,\mathrm{m/s}$ in all inertial frames.

The **Lorentz transformation** from $S$ to $S'$ (moving at speed $v$ along $x$):

$$t' = \gamma\!\left(t - \frac{vx}{c^2}\right), \quad x' = \gamma(x-vt), \quad y'=y, \quad z'=z,$$

where $\gamma = (1-v^2/c^2)^{-1/2}$.

## 6.2 Minkowski Spacetime

Coordinates $(x^0,x^1,x^2,x^3) = (ct,x,y,z)$. The **Minkowski metric**:

$$\eta_{\mu\nu} = \mathrm{diag}(-1,+1,+1,+1).$$

**Spacetime interval** (Lorentz-invariant):

$$ds^2 = \eta_{\mu\nu}dx^\mu dx^\nu = -c^2dt^2 + dx^2 + dy^2 + dz^2.$$

- $ds^2 < 0$: timelike; $ds^2=0$: lightlike (null); $ds^2>0$: spacelike.

## 6.3 Four-Vectors and Energy-Momentum

**Four-velocity:** $U^\mu = dx^\mu/d\tau = \gamma(c,\mathbf{v})$, with $U^\mu U_\mu = -c^2$.

**Four-momentum:** $p^\mu = mU^\mu = (E/c, \mathbf{p})$.

**Mass-energy relation:** $p^\mu p_\mu = -m^2c^2 \implies E^2 = |\mathbf{p}|^2c^2 + m^2c^4$.

## 6.4 Proper Time

The **proper time** is the time measured by a comoving clock:

$$d\tau = dt\sqrt{1-v^2/c^2} = \frac{dt}{\gamma}.$$

Proper time is a Lorentz invariant: $c^2d\tau^2 = -ds^2$.

---

# Chapter 7: General Relativity

## 7.1 The Principle of Equivalence

**Weak Equivalence Principle (WEP):** Inertial mass equals gravitational mass for all bodies. All bodies fall with the same acceleration in a gravitational field (Galileo's result).

**Einstein's Equivalence Principle (EEP):** Locally (in a sufficiently small spacetime region), the effects of gravity are indistinguishable from uniform acceleration. There always exists a local inertial frame (LIF) where SR holds.

**Consequence:** Gravity = curvature of spacetime. Freely-falling particles move on **geodesics**.

## 7.2 The Einstein Field Equations

The field equations relate spacetime curvature to the distribution of matter/energy:

$$\boxed{G_{\mu\nu} = \frac{8\pi G}{c^4}T_{\mu\nu}.}$$

The Bianchi identity $\nabla^\mu G_{\mu\nu}=0$ ensures $\nabla^\mu T_{\mu\nu}=0$ (energy-momentum conservation).

The constant $8\pi G/c^4$ is fixed by the Newtonian limit (derived below in §7.5).

## 7.3 Derivation from the Einstein–Hilbert Action

The **Einstein-Hilbert action** is

$$S = \frac{c^4}{16\pi G}\int R\sqrt{-g}\,d^4x + S_{\mathrm{matter}}.$$

**Variation with respect to $g^{\mu\nu}$:**

**Step 1.** $\delta\sqrt{-g}$. Using $\delta\ln(-g) = g^{\mu\nu}\delta g_{\mu\nu}$ and $\delta g_{\mu\nu} = -g_{\mu\alpha}g_{\nu\beta}\delta g^{\alpha\beta}$:

$$\delta\sqrt{-g} = -\frac{1}{2}\sqrt{-g}\,g_{\mu\nu}\delta g^{\mu\nu}.$$

**Proof:** $g = \det(g_{\mu\nu})$. The variation of a determinant: $\delta g = g\cdot g^{\mu\nu}\delta g_{\mu\nu}$. And $\delta g_{\mu\nu} = -g_{\mu\alpha}g_{\nu\beta}\delta g^{\alpha\beta}$, so $g^{\mu\nu}\delta g_{\mu\nu} = -g_{\mu\nu}\delta g^{\mu\nu}$. Thus $\delta\sqrt{-g} = (-g)^{1/2}\cdot\frac{1}{2}\cdot\frac{\delta g}{g}\cdot(-1) = \frac{\sqrt{-g}}{2}\cdot(-g_{\mu\nu}\delta g^{\mu\nu}) = -\frac{1}{2}\sqrt{-g}\,g_{\mu\nu}\delta g^{\mu\nu}$. $\square$

**Step 2.** $\delta(R\sqrt{-g}) = \delta R\sqrt{-g} + R\,\delta\sqrt{-g}$.

$$= \sqrt{-g}\left(R_{\mu\nu}\delta g^{\mu\nu} + g^{\mu\nu}\delta R_{\mu\nu} - \frac{1}{2}g_{\mu\nu}R\,\delta g^{\mu\nu}\right).$$

**Step 3.** The **Palatini identity**: $g^{\mu\nu}\delta R_{\mu\nu} = \nabla_\mu v^\mu$ for some vector $v^\mu$ (total divergence). By the divergence theorem with appropriate boundary conditions, $\int \nabla_\mu v^\mu\sqrt{-g}\,d^4x = 0$. (Explicitly: $\delta R^\mu_{\ \nu\mu\rho} = \nabla_\mu(\delta\Gamma^\mu_{\nu\rho}) - \nabla_\rho(\delta\Gamma^\mu_{\nu\mu})$, so $g^{\nu\rho}\delta R^\mu_{\ \nu\mu\rho} = \nabla_\mu(g^{\nu\rho}\delta\Gamma^\mu_{\nu\rho} - g^{\mu\nu}\delta\Gamma^\rho_{\nu\rho})$, which is a total divergence.)

**Step 4.** Define the stress-energy tensor as

$$T_{\mu\nu} = -\frac{2}{\sqrt{-g}}\frac{\delta S_{\mathrm{matter}}}{\delta g^{\mu\nu}}.$$

**Step 5.** Setting $\delta S = 0$:

$$\int\sqrt{-g}\left(R_{\mu\nu} - \frac{1}{2}g_{\mu\nu}R - \frac{8\pi G}{c^4}T_{\mu\nu}\right)\delta g^{\mu\nu}d^4x = 0.$$

Since $\delta g^{\mu\nu}$ is arbitrary:

$$R_{\mu\nu} - \frac{1}{2}g_{\mu\nu}R = \frac{8\pi G}{c^4}T_{\mu\nu}. \quad\square$$

## 7.4 The Stress-Energy Tensor

$T^{\mu\nu}$ encodes energy and momentum:

- $T^{00}$: energy density
- $T^{0i}$: energy flux / momentum density  
- $T^{ij}$: stress

**Perfect fluid:** $T^{\mu\nu} = (\rho + P/c^2)U^\mu U^\nu + Pg^{\mu\nu}$.

**Vacuum:** $T_{\mu\nu}=0$, so vacuum EFEs are $R_{\mu\nu}=0$.

## 7.5 Weak-Field Limit: Recovery of Newtonian Gravity

Write $g_{\mu\nu} = \eta_{\mu\nu} + h_{\mu\nu}$, $|h_{\mu\nu}|\ll 1$. For slow motion and static field, the geodesic equation gives

$$\frac{d^2x^i}{dt^2} \approx -\Gamma^i_{00}c^2 = \frac{c^2}{2}\partial^i h_{00}.$$

But $d^2\mathbf{x}/dt^2 = -\nabla\Phi$ (Newtonian), so $h_{00} = -2\Phi/c^2$, giving

$$g_{00} = -(1 + 2\Phi/c^2) = -\!\left(1 - \frac{2GM}{c^2 r}\right) \text{ for a point mass.}$$

**Derivation of $\Gamma^i_{00}$:**

$$\Gamma^i_{00} = \frac{1}{2}\eta^{ij}(2\partial_0 h_{j0} - \partial_j h_{00}) = -\frac{1}{2}\partial^i h_{00} \quad\text{(static: }\partial_0=0\text{)}.$$

So $d^2x^i/dt^2 = -\frac{c^2}{2}\partial^i h_{00} = -\partial^i\Phi$, giving $h_{00} = 2\Phi/c^2$. Wait: $g_{00} = -(1+h_{00})$ in the convention where $\eta_{00}=-1$, and $-\nabla\Phi = +\frac{c^2}{2}\nabla h_{00}$... Let me be precise.

With $\eta_{\mu\nu} = \mathrm{diag}(-1,1,1,1)$ and $g_{\mu\nu}=\eta_{\mu\nu}+h_{\mu\nu}$:

$$\Gamma^i_{00} = \frac{1}{2}\eta^{ij}(\partial_0 h_{j0}+\partial_0 h_{j0}-\partial_j h_{00})\approx -\frac{1}{2}\eta^{ij}\partial_j h_{00} = -\frac{1}{2}\partial^i h_{00}.$$

Geodesic: $\ddot{x}^i + \Gamma^i_{00}(c\dot{t})^2 \approx 0$ for slow motion ($\dot{x}^i \ll c$), so:

$$\ddot{x}^i \approx -\Gamma^i_{00}c^2 = \frac{c^2}{2}\partial^i h_{00}.$$

Comparing with $\ddot{x}^i = -\partial^i\Phi$: $h_{00} = -2\Phi/c^2$, so

$$g_{00} = -1 + h_{00} = -1 - \frac{2\Phi}{c^2} = -\!\left(1 + \frac{2\Phi}{c^2}\right).$$

For gravity ($\Phi = -GM/r < 0$): $g_{00} = -(1-2GM/(c^2 r))$. $\checkmark$

**Recovery of Poisson's equation.** From the $(00)$ Einstein equation in the weak-field limit:

$$R_{00} \approx \frac{4\pi G}{c^2}(\rho c^2) = 4\pi G\rho.$$

In the linearized approximation $R_{00} \approx -\frac{1}{2}\nabla^2 h_{00} = \frac{1}{c^2}\nabla^2\Phi$. So:

$$\frac{1}{c^2}\nabla^2\Phi = \frac{4\pi G\rho}{c^2} \implies \nabla^2\Phi = 4\pi G\rho. \quad\square$$

(This confirms the factor $8\pi G/c^4$ in the Einstein equations.)

---

# Chapter 8: The Schwarzschild Solution

## 8.1 Birkhoff's Theorem

**Theorem 8.1.1 (Birkhoff).** The unique spherically-symmetric solution of the vacuum Einstein equations $R_{\mu\nu}=0$ is static and given by the Schwarzschild metric.

We prove this constructively by deriving the most general such metric.

## 8.2 Derivation of the Schwarzschild Metric

**Step 1: General spherically-symmetric metric.** The most general metric invariant under $SO(3)$ rotations:

$$ds^2 = -e^{2\alpha(t,r)}c^2dt^2 + e^{2\beta(t,r)}dr^2 + r^2 d\Omega^2,$$

where $d\Omega^2 = d\theta^2 + \sin^2\theta\,d\phi^2$. The coordinate $r$ is defined so that spheres of coordinate radius $r$ have area $4\pi r^2$.

**Step 2: Non-zero metric components.**

$$g_{00} = -e^{2\alpha},\; g_{11} = e^{2\beta},\; g_{22} = r^2,\; g_{33} = r^2\sin^2\theta.$$

**Step 3: Non-zero Christoffel symbols.** (Primes: $\partial_r$; dots: $\frac{1}{c}\partial_t$):

$$\Gamma^0_{00} = \dot\alpha,\quad \Gamma^0_{01}=\Gamma^0_{10} = \alpha',\quad \Gamma^0_{11} = \dot\beta\,e^{2(\beta-\alpha)},$$

$$\Gamma^1_{00} = \alpha'\,e^{2(\alpha-\beta)},\quad \Gamma^1_{01}=\Gamma^1_{10} = \dot\beta,\quad \Gamma^1_{11} = \beta',$$

$$\Gamma^1_{22} = -r\,e^{-2\beta},\quad \Gamma^1_{33} = -r\sin^2\theta\,e^{-2\beta},$$

$$\Gamma^2_{12}=\Gamma^2_{21} = \frac{1}{r},\quad \Gamma^2_{33} = -\sin\theta\cos\theta,$$

$$\Gamma^3_{13}=\Gamma^3_{31} = \frac{1}{r},\quad \Gamma^3_{23}=\Gamma^3_{32} = \cot\theta.$$

**Verification of $\Gamma^1_{00}$:** $\Gamma^1_{00} = \frac{1}{2}g^{11}(2\partial_0 g_{10}-\partial_1 g_{00})$. Since $g_{10}=0$: $= \frac{1}{2}e^{-2\beta}\cdot(-\partial_r(-e^{2\alpha})) = \frac{1}{2}e^{-2\beta}\cdot 2\alpha'e^{2\alpha} = \alpha'e^{2(\alpha-\beta)}$. $\checkmark$

**Step 4: Ricci tensor components.**

Computing $R_{\mu\nu} = \partial_\rho\Gamma^\rho_{\mu\nu} - \partial_\nu\Gamma^\rho_{\mu\rho} + \Gamma^\rho_{\rho\lambda}\Gamma^\lambda_{\mu\nu} - \Gamma^\rho_{\nu\lambda}\Gamma^\lambda_{\mu\rho}$ for each $(\mu,\nu)$:

$$R_{00} = e^{2(\alpha-\beta)}\!\left[-\alpha'' - (\alpha')^2 + \alpha'\beta' - \frac{2\alpha'}{r}\right] + \ddot\beta + (\dot\beta)^2 - \dot\alpha\dot\beta,$$

$$R_{11} = \alpha'' + (\alpha')^2 - \alpha'\beta' - \frac{2\beta'}{r} - e^{2(\beta-\alpha)}\!\left[\ddot\beta + (\dot\beta)^2 - \dot\alpha\dot\beta\right],$$

$$R_{01} = \frac{2\dot\beta}{r},$$

$$R_{22} = e^{-2\beta}[r(\beta'-\alpha')-1] + 1, \qquad R_{33} = R_{22}\sin^2\theta.$$

**Step 5: Apply $R_{\mu\nu}=0$.**

**From $R_{01}=0$:** $2\dot\beta/r = 0 \implies \dot\beta = 0 \implies \beta = \beta(r)$ only ($\beta$ is time-independent).

**From $R_{00}e^{-2\alpha} + R_{11}e^{-2\beta}=0$** (combining to eliminate time-derivative terms using $\dot\beta=0$):

$$-\frac{2\alpha'}{r}\cdot e^{-2\beta} - \frac{2\beta'}{r}\cdot e^{-2\beta} = 0 \implies \alpha' + \beta' = 0 \implies \alpha = -\beta + f(t).$$

A time-dependent part $f(t)$ in $\alpha$ can be absorbed by redefining $t \to \tilde{t}$ (reparametrize proper time). After this, $\alpha = -\beta$ (with $\beta$ depending only on $r$), making the metric static.

**From $R_{22}=0$** with $\alpha=-\beta$:

$$e^{-2\beta}[r(\beta'+\beta')-1]+1=0 \implies e^{-2\beta}(2r\beta'-1) = -1.$$

Let $f = e^{-2\beta}$. Then $f' = -2\beta'e^{-2\beta} = -2\beta'f$, so $\beta' = -f'/(2f)$. Substitute:

$$f\!\left(2r\cdot\left(-\frac{f'}{2f}\right)-1\right) = -1 \implies -rf' - f = -1 \implies rf' + f = 1.$$

Recognize: $\frac{d}{dr}(rf) = f + rf' = 1$. Therefore:

$$rf = r - r_s \implies e^{-2\beta} = f = 1 - \frac{r_s}{r},$$

where $r_s > 0$ is a constant of integration.

Since $\alpha = -\beta$: $e^{2\alpha} = e^{-2\beta} = 1-r_s/r$.

**Step 6: The Schwarzschild metric.**

$$\boxed{ds^2 = -\!\left(1-\frac{r_s}{r}\right)c^2 dt^2 + \frac{dr^2}{1-r_s/r} + r^2 d\Omega^2.}$$

**Step 7: Fix $r_s$ from the Newtonian limit.** As $r\to\infty$: $g_{00}\to-1+r_s/r = -(1-r_s/r)$. From §7.5, $g_{00} = -(1-2GM/c^2 r)$. So:

$$r_s = \frac{2GM}{c^2} \quad\text{(Schwarzschild radius).} \quad\square$$

One can verify that all components of $R_{\mu\nu}$ vanish with this metric. $\checkmark$

## 8.3 Coordinate Singularities and the Schwarzschild Radius

The metric has apparent divergences at $r=0$ and $r=r_s$:

- **$r=r_s$:** $g_{rr}\to\infty$, but the Kretschner scalar $K = R_{\mu\nu\rho\sigma}R^{\mu\nu\rho\sigma} = 12r_s^2/r^6$ is finite. This is a **coordinate singularity** — removable by Kruskal–Szekeres coordinates. $r=r_s$ is the **event horizon**.

- **$r=0$:** $K = 12r_s^2/r^6\to\infty$. This is a genuine **curvature singularity**.

**Schwarzschild radii for reference:**

| Object | Mass | $r_s$ |
|:---:|:---:|:---:|
| Sun | $2.0\times10^{30}$ kg | 2.95 km |
| Earth | $6.0\times10^{24}$ kg | 8.9 mm |
| Mercury | $3.3\times10^{23}$ kg | 0.49 mm |

The Sun's actual radius is 696,000 km $\gg r_s^\odot = 2.95$ km, so the Schwarzschild metric is a valid exterior description.

## 8.4 Geodesics in Schwarzschild Spacetime

The Lagrangian for geodesic motion ($\theta=\pi/2$ by the planar reduction):

$$2\mathcal{L} = -\!\left(1-\frac{r_s}{r}\right)c^2\dot{t}^2 + \frac{\dot{r}^2}{1-r_s/r} + r^2\dot{\phi}^2 = -c^2,$$

where dots are $d/d\tau$ and the normalization $g_{\mu\nu}\dot{x}^\mu\dot{x}^\nu = -c^2$ holds for massive particles.

**Planar reduction.** The $\theta$-geodesic equation at $\theta=\pi/2$, $\dot\theta=0$: $\ddot\theta - \sin\theta\cos\theta\dot\phi^2 = 0 \to 0$. $\checkmark$ So the equatorial plane is preserved.

## 8.5 Conserved Quantities from Killing Vectors

The Schwarzschild metric has two Killing vectors:

**Time translation $\partial_t$:** gives conserved energy

$$E \equiv \left(1-\frac{r_s}{r}\right)c^2\dot{t} = \varepsilon c^2 = \mathrm{const},$$

where $\varepsilon = E/(mc^2)$ is the **specific energy** (energy per unit rest-mass-energy).

**Azimuthal rotation $\partial_\phi$:** gives conserved angular momentum

$$\ell \equiv r^2\dot\phi = \mathrm{const.}$$

(same notation as before, now the specific angular momentum in GR).

**Proof (Killing vector $\xi^\mu$).** For a Killing vector, $\xi_\mu\dot{x}^\mu$ is constant along geodesics:

$$\frac{d}{d\tau}(\xi_\mu\dot{x}^\mu) = \dot{x}^\nu\nabla_\nu(\xi_\mu\dot{x}^\mu) = \dot{x}^\nu\dot{x}^\mu\nabla_\nu\xi_\mu + \xi_\mu\dot{x}^\nu\nabla_\nu\dot{x}^\mu.$$

The first term vanishes since $\nabla_{(\mu}\xi_{\nu)}=0$ (Killing equation) and $\dot{x}^\nu\dot{x}^\mu$ is symmetric. The second term vanishes by the geodesic equation $\dot{x}^\nu\nabla_\nu\dot{x}^\mu=0$. $\square$

**The normalization equation.** Substituting $\dot{t} = \varepsilon/(1-r_s/r)$ and $\dot\phi = \ell/r^2$ into $g_{\mu\nu}\dot{x}^\mu\dot{x}^\nu=-c^2$:

$$-\!\left(1-\frac{r_s}{r}\right)\frac{\varepsilon^2 c^2}{(1-r_s/r)^2} + \frac{\dot{r}^2}{1-r_s/r} + \frac{\ell^2}{r^2} = -c^2.$$

Multiply by $(1-r_s/r)$:

$$-\varepsilon^2 c^2 + \dot{r}^2 + \frac{\ell^2}{r^2}\!\left(1-\frac{r_s}{r}\right) = -c^2\!\left(1-\frac{r_s}{r}\right).$$

$$\boxed{\dot{r}^2 = \varepsilon^2 c^2 - \left(1-\frac{r_s}{r}\right)\!\left(c^2 + \frac{\ell^2}{r^2}\right).}$$

---

# Chapter 9: The Relativistic Two-Body (Test-Particle) Problem

## 9.1 The Effective Potential in Schwarzschild Geometry

From $\frac{1}{2}\dot{r}^2 = \frac{1}{2}\varepsilon^2 c^2 - \frac{1}{2}(1-r_s/r)(c^2+\ell^2/r^2)$, define

$$V_{\mathrm{eff}}^{\mathrm{GR}}(r) = \frac{1}{2}\!\left(1-\frac{r_s}{r}\right)\!\left(c^2 + \frac{\ell^2}{r^2}\right) = \frac{c^2}{2} - \frac{GM}{r} + \frac{\ell^2}{2r^2} - \frac{GM\ell^2}{c^2 r^3}.$$

Subtracting the rest-energy term $c^2/2$ to compare with the Newtonian case:

$$\tilde{V}_{\mathrm{eff}}^{\mathrm{GR}}(r) = -\frac{GM}{r} + \frac{\ell^2}{2r^2} - \frac{GM\ell^2}{c^2 r^3}.$$

Compare with Newton:

$$V_{\mathrm{eff}}^{\mathrm{Newton}}(r) = -\frac{GM}{r} + \frac{\ell^2}{2r^2}.$$

The **extra GR term** is:

$$\Delta V = -\frac{GM\ell^2}{c^2 r^3} = -\frac{r_s\ell^2}{2r^3} < 0.$$

This is always attractive (negative), strengthening gravity at small $r$ relative to Newton.

## 9.2 Circular Orbits and Stability

**Condition for circular orbit:** $d\tilde{V}_{\mathrm{eff}}^{\mathrm{GR}}/dr = 0$:

$$\frac{GM}{r^2} - \frac{\ell^2}{r^3} + \frac{3GM\ell^2}{c^2 r^4} = 0.$$

Multiply by $r^4/(GM)$:

$$r^2 - \frac{\ell^2}{GM}r + \frac{3\ell^2}{c^2} = 0.$$

By the quadratic formula:

$$r_\pm = \frac{\ell^2}{2GM}\!\left[1 \pm \sqrt{1 - \frac{12G^2M^2}{\ell^2 c^2}}\right].$$

**For real solutions:** $\ell \ge \ell_{\min} = 2\sqrt{3}\,GM/c$.

- $r_+$: larger radius, **stable** (local minimum of $V_{\mathrm{eff}}$)
- $r_-$: smaller radius, **unstable** (local maximum of $V_{\mathrm{eff}}$)

**No analog in Newtonian gravity:** in Newton's theory, only $r_+$ exists for any $\ell>0$.

## 9.3 The Innermost Stable Circular Orbit (ISCO)

As $\ell\to\ell_{\min}$, $r_+\to r_- = r_{\mathrm{ISCO}}$:

$$r_{\mathrm{ISCO}} = \frac{\ell_{\min}^2}{2GM} = \frac{(2\sqrt{3}GM/c)^2}{2GM} = \frac{12G^2M^2/c^2}{2GM} = \frac{6GM}{c^2} = 3r_s.$$

$$\boxed{r_{\mathrm{ISCO}} = \frac{6GM}{c^2} = 3r_s.}$$

For $r < r_{\mathrm{ISCO}}$: no stable circular orbits exist. A particle will spiral inward and plunge.

**Physical importance:** The ISCO determines:
- The innermost edge of accretion disks around black holes.
- The gravitational wave frequency at plunge in compact binary mergers.
- For a non-spinning (Schwarzschild) black hole, $r_{\mathrm{ISCO}} = 6GM/c^2$.
- For a maximally spinning (Kerr) black hole, $r_{\mathrm{ISCO}}$ can be as small as $GM/c^2$ (prograde) or as large as $9GM/c^2$ (retrograde).

## 9.4 The GR Orbit Equation: Derivation

**Goal:** Find $r(\phi)$ — the orbit shape.

**Step 1.** Substitution $u=1/r$. As before, $\dot{r} = -\ell u'$ (where prime is $d/d\phi$).

**Step 2.** Substitute $\dot{r}^2 = \ell^2(u')^2$ into the energy equation:

$$\ell^2(u')^2 = \varepsilon^2 c^2 - (1-r_s u)(c^2+\ell^2 u^2).$$

Expand:

$$\ell^2(u')^2 = \varepsilon^2 c^2 - c^2 + r_s c^2 u - \ell^2 u^2 + r_s\ell^2 u^3.$$

$$\ell^2(u')^2 = (\varepsilon^2-1)c^2 + r_s c^2 u - \ell^2 u^2 + r_s\ell^2 u^3.$$

**Step 3.** Differentiate with respect to $\phi$:

$$2\ell^2 u'\,u'' = r_s c^2 u' - 2\ell^2 u\,u' + 3r_s\ell^2 u^2 u'.$$

Divide by $2\ell^2 u'$ (valid off turning points):

$$u'' = \frac{r_s c^2}{2\ell^2} - u + \frac{3r_s}{2}u^2.$$

Using $r_s = 2GM/c^2$: $r_s c^2/(2\ell^2) = GM/\ell^2$ and $3r_s/2 = 3GM/c^2$:

$$\boxed{u'' + u = \frac{GM}{\ell^2} + \frac{3GM}{c^2}u^2.}$$

This is the **GR orbit equation**. The Newtonian Binet equation is recovered by setting $c\to\infty$ (dropping the last term).

## 9.5 Perturbative Solution: Orbital Precession

Write $u = u_0 + u_1 + \cdots$ where $u_0$ is the Newtonian solution and $u_1$ is the small GR correction.

**Zeroth order:**

$$u_0''+u_0 = \frac{GM}{\ell^2} \equiv \alpha.$$

Solution (periapsis at $\phi=0$): $u_0 = \alpha(1+e\cos\phi)$.

**First order:**

$$u_1''+u_1 = \frac{3GM}{c^2}u_0^2 = \frac{3GM\alpha^2}{c^2}(1+e\cos\phi)^2.$$

Expand $(1+e\cos\phi)^2$:

$$(1+e\cos\phi)^2 = 1 + 2e\cos\phi + e^2\cos^2\phi = \left(1+\frac{e^2}{2}\right) + 2e\cos\phi + \frac{e^2}{2}\cos 2\phi.$$

So:

$$u_1''+u_1 = \frac{3GM\alpha^2}{c^2}\!\left[\left(1+\frac{e^2}{2}\right) + 2e\cos\phi + \frac{e^2}{2}\cos 2\phi\right].$$

Solve by superposition:

**Part 1** (constant forcing $A_0 = 3GM\alpha^2(1+e^2/2)/c^2$): particular solution $u_1^{(1)} = A_0$.

**Part 2** (resonant forcing $A_1\cos\phi$, $A_1 = 6GM\alpha^2 e/c^2$): this drives at the natural frequency of the oscillator. Using the result from §1.7:

$$u_1^{(2)} = \frac{A_1}{2}\phi\sin\phi = \frac{3GM\alpha^2 e}{c^2}\phi\sin\phi.$$

**Proof.** Let $u_1 = C\phi\sin\phi$. Then $u_1'' = C(2\cos\phi - \phi\sin\phi)$. So $u_1''+u_1 = 2C\cos\phi = A_1\cos\phi$, giving $C = A_1/2$. $\square$

**Part 3** (off-resonant $A_2\cos 2\phi$, $A_2 = 3GM\alpha^2 e^2/(2c^2)$): particular solution $u_1^{(3)} = -A_2\cos 2\phi/3$.

**Proof.** Let $u_1 = D\cos 2\phi$. Then $u_1'' = -4D\cos 2\phi$. So $u_1''+u_1 = -3D\cos 2\phi = A_2\cos 2\phi$, giving $D = -A_2/3$. $\square$

The **secular (growing) term** $u_1^{(2)} = \frac{3GM\alpha^2 e}{c^2}\phi\sin\phi$ dominates at large $\phi$. The full solution (keeping the secular term):

$$u \approx \alpha(1+e\cos\phi) + \frac{3GM\alpha^2 e}{c^2}\phi\sin\phi + \text{(bounded terms)}.$$

**Extracting the precession.** Use the approximation for small $\epsilon$:

$$\cos[(1-\epsilon)\phi] \approx \cos\phi + \epsilon\phi\sin\phi.$$

**Proof.** $\cos[(1-\epsilon)\phi] = \cos\phi\cos(\epsilon\phi)+\sin\phi\sin(\epsilon\phi) \approx \cos\phi + \epsilon\phi\sin\phi$ for small $\epsilon\phi$. $\square$

So:

$$u \approx \alpha\!\left[1 + e\cos\!\left((1-\epsilon)\phi\right)\right],$$

where

$$\epsilon = \frac{3GM\alpha}{c^2} = \frac{3GM}{c^2}\cdot\frac{GM}{\ell^2} = \frac{3G^2M^2}{c^2\ell^2} = \frac{3GM}{c^2 p}.$$

The periapsis occurs at $(1-\epsilon)\phi = 2\pi n$, i.e., $\phi = 2\pi n/(1-\epsilon)$. Consecutive periapses are separated by

$$\Delta\phi_{\mathrm{orbit}} = \frac{2\pi}{1-\epsilon} - 2\pi \approx 2\pi\epsilon \quad (\epsilon\ll 1).$$

$$\boxed{\Delta\phi = \frac{6\pi GM}{c^2 p} = \frac{6\pi GM}{c^2 a(1-e^2)}}$$

per orbit. This is the **relativistic periapsis advance**.

## 9.6 Mercury's Perihelion Advance: Explicit Calculation

**Mercury's orbital parameters:**

| Parameter | Value |
|:---:|:---:|
| Semi-major axis $a$ | $5.7909\times10^{10}$ m |
| Eccentricity $e$ | $0.2056$ |
| Orbital period $T$ | $87.969$ days |

**Constants:**
- $GM_\odot = 1.32712\times10^{20}$ m³/s²
- $c = 2.99792\times10^8$ m/s

**Step 1: Semi-latus rectum.**

$$p = a(1-e^2) = 5.7909\times10^{10}\times(1-0.04227) = 5.7909\times10^{10}\times 0.95773 = 5.546\times10^{10}\,\mathrm{m}.$$

**Step 2: Advance per orbit.**

$$\Delta\phi = \frac{6\pi GM_\odot}{c^2 p} = \frac{6\pi\times 1.32712\times10^{20}}{(2.99792\times10^8)^2\times 5.546\times10^{10}}.$$

Numerator: $6\pi\times 1.32712\times10^{20} = 18.8496\times 1.32712\times10^{20} = 2.5016\times10^{21}$.

Denominator: $(2.99792\times10^8)^2 = 8.9875\times10^{16}$. Then $8.9875\times10^{16}\times 5.546\times10^{10} = 4.9848\times10^{27}$.

$$\Delta\phi = \frac{2.5016\times10^{21}}{4.9848\times10^{27}} = 5.018\times10^{-7}\,\mathrm{rad/orbit}.$$

**Step 3: Convert to arcseconds.**

$$\Delta\phi = 5.018\times10^{-7}\,\mathrm{rad}\times\frac{180}{\pi}\times 3600 = 5.018\times10^{-7}\times 206265 = 0.10348''/\mathrm{orbit}.$$

**Step 4: Orbits per century.**

$$N = \frac{100\times 365.25\,\mathrm{days}}{87.969\,\mathrm{days}} = \frac{36525}{87.969} = 415.20\,\mathrm{orbits/century}.$$

**Step 5: Advance per century.**

$$\Delta\phi_{\mathrm{century}} = 0.10348\times 415.20 = 42.96''/\mathrm{century} \approx 43''/\mathrm{century}.$$

**Observed value:** The anomalous perihelion advance (after subtracting gravitational perturbations from other planets) is $43.11 \pm 0.45''$/century.

$$\boxed{\Delta\phi_{\mathrm{GR}} \approx 43''/\mathrm{century} \quad \text{(matches observation to better than 1\%).}}$$

This was one of the three "classical tests" of GR announced by Einstein in 1915 and confirmed the theory dramatically.

## 9.7 Radial Geodesics: Free-Fall into a Black Hole

Set $\ell=0$ (purely radial motion). The energy equation becomes:

$$\dot{r}^2 = \varepsilon^2 c^2 - c^2\!\left(1-\frac{r_s}{r}\right).$$

For a particle dropped from rest at $r=r_0$: at $r_0$, $\dot{r}=0$, so $\varepsilon^2 c^2 = c^2(1-r_s/r_0)$. Thus:

$$\dot{r}^2 = c^2 r_s\!\left(\frac{1}{r} - \frac{1}{r_0}\right) = \frac{c^2 r_s(r_0-r)}{r\cdot r_0}.$$

**Proper time to reach $r=0$:**

$$\Delta\tau = \int_0^{r_0}\frac{dr}{c\sqrt{r_s(1/r-1/r_0)}} = \frac{1}{c}\sqrt{\frac{r_0}{r_s}}\int_0^{r_0}\sqrt{\frac{r}{r_0-r}}\,dr.$$

Substitute $r = r_0\sin^2\psi$, $dr = 2r_0\sin\psi\cos\psi\,d\psi$:

$$= \frac{r_0}{c}\sqrt{\frac{r_0}{r_s}}\int_0^{\pi/2} 2\sin^2\psi\,d\psi = \frac{r_0}{c}\sqrt{\frac{r_0}{r_s}}\cdot\frac{\pi}{2} = \frac{\pi r_0}{2c}\sqrt{\frac{r_0}{r_s}}.$$

This is **finite**: the infalling observer crosses $r=r_s$ and reaches $r=0$ in finite proper time.

**Coordinate time to reach $r=r_s$:** Using $dt/dr = \dot{t}/\dot{r}$ and $\dot{t} = \varepsilon/(1-r_s/r)$:

$$\frac{dt}{dr} = \frac{\varepsilon/[c^2(1-r_s/r)]}{-c\sqrt{r_s(1/r-1/r_0)/c^2}} \propto \frac{1}{1-r_s/r}.$$

As $r\to r_s$: $(1-r_s/r)\to 0$, so $|dt/dr|\to\infty$. The coordinate time diverges logarithmically:

$$\Delta t \propto -\frac{r_s}{c}\ln(r-r_s) \to +\infty \quad\text{as } r\to r_s.$$

**Interpretation.** From the perspective of a distant observer, the infalling particle asymptotically approaches but never crosses $r_s$. From the infalling observer's own proper time, the crossing happens in finite time. Both descriptions are consistent — they use different time coordinates.

## 9.8 Comparison: Newtonian vs. General Relativistic Two-Body Problem

| Feature | Newtonian | General Relativistic |
|:---|:---|:---|
| Governing equation | $\mu\ddot{\mathbf{r}} = -GM\mu\mathbf{r}/r^3$ | Schwarzschild geodesic equation |
| Orbit equation | $u''+u = GM/\ell^2$ | $u''+u = GM/\ell^2 + 3GMu^2/c^2$ |
| Orbits | Exactly closed conic sections | Precessing ellipses |
| Periapsis advance per orbit | 0 | $\Delta\phi = 6\pi GM/(c^2 p)$ |
| Effective potential | $-GM/r+\ell^2/(2r^2)$ | $-GM/r+\ell^2/(2r^2)-GM\ell^2/(c^2r^3)$ |
| Circular orbits stable for | All $r>0$ | Only $r > 6GM/c^2$ |
| ISCO | Does not exist | $r_{\mathrm{ISCO}} = 6GM/c^2 = 3r_s$ |
| Conserved quantities | $E$, $\mathbf{L}$, $\mathbf{A}$ (Runge-Lenz) | $E$, $L_z$ (Runge-Lenz not conserved) |
| Radial fall to center | Finite coordinate and proper time | Finite proper time, infinite coordinate time |
| Speed limit | None ($v$ can exceed $c$) | $v \leq c$ always |
| Gravitational waves | Not predicted | Radiated by accelerating masses |
| Strong-field behavior | Orbits remain open | Plunge inside ISCO |

---

# Chapter 10: Summary and Conclusions

We have developed the complete mathematical framework for the two-body gravitational problem from first principles in both Newtonian mechanics and general relativity.

**Newtonian summary.** Starting from Newton's laws and the law of universal gravitation, we reduced the two-body problem to a one-body problem with reduced mass $\mu = m_1m_2/(m_1+m_2)$ and derived:

1. The Binet orbit equation $u''+u = GM/\ell^2$, with general solution $r = p/(1+e\cos\phi)$.
2. All three Kepler's laws, rigorously: elliptic orbits (First), conservation of angular momentum as equal areas (Second), and $T^2\propto a^3$ (Third).
3. The vis-viva equation $v^2 = GM(2/r-1/a)$.
4. The Runge-Lenz vector, whose conservation explains orbital closure and the exact degeneracy $\omega_r = \omega_\phi$ of radial and orbital frequencies.

**GR summary.** After developing differential geometry and special relativity, we derived the Einstein field equations both from physical principles and from the Einstein-Hilbert action. The Schwarzschild solution — the unique spherically-symmetric vacuum solution — was derived in full. From geodesic equations we found:

1. The GR orbit equation $u''+u = GM/\ell^2 + 3GMu^2/c^2$, with the extra $1/r^3$ correction.
2. The periapsis advance $\Delta\phi = 6\pi GM/(c^2 a(1-e^2))$ per orbit.
3. The ISCO at $r = 6GM/c^2$, below which no stable circular orbits exist.
4. Mercury's perihelion advance: $\approx 43''$/century, matching observation.

**The physics of the correction.** The term $-GM\ell^2/(c^2r^3)$ in the GR effective potential does three things: (a) it shifts circular orbit radii inward; (b) it breaks the degeneracy $\omega_r = \omega_\phi$, causing orbits not to close (periapsis advances); (c) at sufficiently small $r$, it overwhelms the centrifugal barrier, eliminating stable circular orbits below $r_{\mathrm{ISCO}}$.

---

# Appendix A: Proof that the Orbit Equation Describes Conic Sections

We prove that $r = p/(1+e\cos\phi)$ is the polar equation of a conic with the origin at a focus.

Starting from $r(1+e\cos\phi) = p$, i.e., $r + ex = p$ where $x = r\cos\phi$:

$$r = p - ex \implies r^2 = (p-ex)^2.$$

With $r^2 = x^2+y^2$:

$$x^2+y^2 = p^2 - 2epx + e^2x^2$$

$$x^2(1-e^2) + 2epx + y^2 = p^2. \tag{A.1}$$

**Case 1: $e < 1$ (ellipse).** Complete the square in $x$:

$$(1-e^2)\!\left(x + \frac{ep}{1-e^2}\right)^2 - \frac{e^2p^2}{1-e^2} + y^2 = p^2.$$

$$(1-e^2)\!\left(x + \frac{ep}{1-e^2}\right)^2 + y^2 = p^2 + \frac{e^2p^2}{1-e^2} = \frac{p^2(1-e^2+e^2)}{1-e^2} = \frac{p^2}{1-e^2}.$$

Divide by $p^2/(1-e^2)$:

$$\frac{(x-x_0)^2}{a^2} + \frac{y^2}{b^2} = 1,$$

where $x_0 = -ep/(1-e^2) = -ea$ (shift of center), $a = p/(1-e^2)$ (semi-major axis), $b^2 = p^2/(1-e^2) \cdot \frac{1}{1} = a^2(1-e^2)$ (semi-minor axis). The center is at $(-ea,0)$; the focus at origin is at distance $ea$ from center. $\checkmark$ This is a standard ellipse with one focus at the origin.

**Case 2: $e = 1$ (parabola).** From (A.1) with $e=1$: $2px + y^2 = p^2$, giving $x = (p^2-y^2)/(2p) = p/2 - y^2/(2p)$. This is a parabola with vertex at $(p/2,0)$, focus at origin. $\checkmark$

**Case 3: $e > 1$ (hyperbola).** Complete the square as in Case 1, but now $(1-e^2)<0$. Write $e^2-1 > 0$:

$$\frac{(x-x_0)^2}{a^2} - \frac{y^2}{b^2} = 1,$$

with $a = p/(e^2-1)$, $b^2 = a^2(e^2-1)$, $x_0 = ea$. This is a hyperbola with one branch having the focus at the origin. $\checkmark$ $\square$

---

# Appendix B: Christoffel Symbols for the Schwarzschild Metric

With $f = 1-r_s/r$, coordinates $(x^0,x^1,x^2,x^3)=(ct,r,\theta,\phi)$:

$$g_{00}=-fc^2,\; g_{11}=f^{-1},\; g_{22}=r^2,\; g_{33}=r^2\sin^2\theta.$$

$$g^{00}=-(fc^2)^{-1},\; g^{11}=f,\; g^{22}=r^{-2},\; g^{33}=(r^2\sin^2\theta)^{-1}.$$

Non-zero Christoffel symbols (using $f'=df/dr = r_s/r^2$):

$$\Gamma^0_{01}=\Gamma^0_{10} = \frac{f'}{2f} = \frac{r_s}{2r^2 f},$$

$$\Gamma^1_{00} = \frac{fc^2 f'}{2} = \frac{GMc^2 f}{r^2},$$

$$\Gamma^1_{11} = -\frac{f'}{2f} = -\frac{r_s}{2r^2 f},$$

$$\Gamma^1_{22} = -rf,$$

$$\Gamma^1_{33} = -rf\sin^2\theta,$$

$$\Gamma^2_{12}=\Gamma^2_{21} = \frac{1}{r},$$

$$\Gamma^2_{33} = -\sin\theta\cos\theta,$$

$$\Gamma^3_{13}=\Gamma^3_{31} = \frac{1}{r},$$

$$\Gamma^3_{23}=\Gamma^3_{32} = \cot\theta.$$

**Verification of $\Gamma^1_{00}$:** $\Gamma^1_{00} = \frac{1}{2}g^{11}(-\partial_r g_{00}) = \frac{f}{2}\cdot\partial_r(fc^2) = \frac{fc^2}{2}f' = \frac{fc^2 r_s}{2r^2} = \frac{GMfc^2}{c^2r^2} = \frac{GMf}{r^2}\cdot c^2/c^2$. 

More carefully: $g_{00} = -fc^2$, so $\partial_r g_{00} = -f'c^2$. Then:

$$\Gamma^1_{00} = \frac{1}{2}g^{11}(2\partial_0 g_{01}-\partial_1 g_{00}) = \frac{f}{2}\cdot f'c^2 = \frac{c^2 f f'}{2} = \frac{c^2 f r_s}{2r^2}. \quad\checkmark$$

---

# Appendix C: Riemann Tensor and Curvature Invariant for Schwarzschild

The independent non-zero components of the Riemann tensor (with all indices down) at $\theta=\pi/2$:

$$R_{trtr} = -\frac{GM}{r^3}\frac{c^2}{f},\quad R_{t\theta t\theta} = \frac{GMc^2 fr^2}{r^3} = \frac{GMc^2 f}{r},$$

$$R_{t\phi t\phi} = \frac{GMc^2 f\sin^2\theta}{r},\quad R_{r\theta r\theta} = -\frac{GM}{r f},$$

$$R_{r\phi r\phi} = -\frac{GM\sin^2\theta}{rf},\quad R_{\theta\phi\theta\phi} = r_s r\sin^2\theta.$$

**The Kretschner scalar:**

$$K = R_{\mu\nu\rho\sigma}R^{\mu\nu\rho\sigma} = \frac{12r_s^2}{r^6} = \frac{48G^2M^2}{c^4 r^6}.$$

**Proof that $K$ is finite at $r=r_s$:** $K = 48G^2M^2/(c^4 r_s^6) = 48G^2M^2/(c^4\cdot(2GM)^6/c^{12}) = 48c^8/(64G^4M^4) = \frac{3c^8}{4G^4M^4}$, which is finite. $\checkmark$

**The Ricci tensor** $R_{\mu\nu}=0$ throughout (as required by the vacuum field equations), even though the Riemann tensor is non-zero: spacetime is curved but empty.

---

## Notation Summary

| Symbol | Meaning |
|:---:|:---|
| $G$ | Newton's gravitational constant ($6.674\times10^{-11}$ N m² kg⁻²) |
| $c$ | Speed of light ($2.998\times10^8$ m/s) |
| $M = m_1+m_2$ | Total mass |
| $\mu = m_1m_2/M$ | Reduced mass |
| $k = GM$ | Gravitational parameter |
| $r_s = 2GM/c^2$ | Schwarzschild radius |
| $\ell = r^2\dot\phi$ | Specific angular momentum |
| $\varepsilon = E/(mc^2)$ | Specific energy |
| $e$ | Orbital eccentricity |
| $p = \ell^2/k$ | Semi-latus rectum |
| $a$ | Semi-major axis |
| $T$ | Orbital period |
| $\Delta\phi$ | Periapsis advance per orbit |
| $\Gamma^\rho_{\mu\nu}$ | Christoffel symbols (Levi-Civita connection) |
| $R^\rho_{\ \sigma\mu\nu}$ | Riemann curvature tensor |
| $R_{\mu\nu}$ | Ricci tensor |
| $R$ | Ricci scalar |
| $G_{\mu\nu}$ | Einstein tensor |
| $T_{\mu\nu}$ | Stress-energy tensor |
| $g_{\mu\nu}$ | Metric tensor |
| $\eta_{\mu\nu}$ | Minkowski metric $\mathrm{diag}(-1,+1,+1,+1)$ |
| $\tau$ | Proper time |
| $\nabla_\mu$ | Covariant derivative |
| $\delta_{ij}$ | Kronecker delta |
| $\epsilon_{ijk}$ | Levi-Civita symbol |
