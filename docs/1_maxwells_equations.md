# Maxwell's Equations - Building blocks

<p align=justify>
Before starting to solve any electromagnetism problem, we must first write down the equations that enable us to solve any of these problems - Maxwell's equations. These equations are the building blocks of any electromagnetic problem. Behold the four wonderful equations:
</p>

## Ampere's Law
(Varying magnetic fields can induce electric currents, producing orthogonal electric fields)
$$\nabla \times \vec{H} = \vec{J} + \frac{\partial \vec{D}}{\partial t}$$

## Faraday's Law
(Varying electric fields can induce orthogonal magnetic flux density fields)
$$\nabla \times \vec{E} = -\frac{\partial \vec{B}}{\partial t}$$

## Poisson's Equation
(There can be electric field sources and sinks - electric charges)
$$\nabla \cdot \vec{D} = \rho$$

## Condition of Solenoidal Magnetic Flux Density
(There are no sources or sinks of magnetic flux density. In other words, magnetic fields are always closed.)

$$\nabla \cdot \vec{B} = 0$$

<p align=justify>Here H is the magnetic field, J is the current density, D is the electric displacement, E is the electric field, B is the magnetic flux density, ρ is the electric charge density, and t denotes the time variable.</p>

## Constitutive Relations

### Magnetic Field:
$$\vec{H} = \frac{\vec{H}}{\mu} - \vec{M}$$

where $\vec{M}$ is the magnetization of matter vector.

### Electric Field:

$$\vec{D} = \epsilon \vec{E} + \vec{P}$$

where $\vec{P}$ is the polarization of matter vector.

## Important Note:
<p align=justify>In these notebooks, all problems will be solved by restricting our attention to linear, isotropic and nondispersive materials for which the constitutive relations are given by:</p>

$$\vec{D} = \epsilon \vec{E}$$

$$\vec{B} = \mu \vec{H}$$

## All together now: 

<p align=justify> Maxwell's equations were actually 19, but it was Heaviside that was able to condense them to just four equations and the additional two constitutive relations. The four equations shown above are represented in their time-domain differential form, but Heaviside also demonstrated that there are actually other possible forms to represent them. All these forms are represented in the table below.</p>

|                  | Integral Form | Differential Form |
|------------------|-------------------|---------------|
| Time Domain |$$ \oiint_{\partial\Omega} \vec{D}\cdot\vec{dS} = \iiint_\Omega \rho \hspace{0.1cm}dV \\ \oiint_{\partial\Omega}\vec{B}\cdot\vec{dS}=0 \\ \oint_{\partial \Gamma}\vec{E}\cdot \vec{dl}=-\frac{\partial}{\partial t}\iint_{\Gamma}\vec{B}\cdot \vec{dS} \\ \oint_{\partial \Gamma} \vec{B} \cdot \vec{dl} = \iint_\Gamma \vec{J}\cdot\vec{dS} + \frac{\partial}{\partial t}\iint_\Gamma \vec{D} \cdot \vec{dS} $$|$$ \nabla \cdot \vec{D} = \rho \\ \nabla \cdot \vec{B} = 0 \\ \nabla \times \vec{E} = -\frac{\partial \vec{B}}{\partial t} \\ \nabla \times \vec{H} = \vec{J} + \frac{\partial \vec{D}}{\partial t}$$|
| Frequency Domain |$$ \oiint_{\partial\Omega} \vec{D}(\omega)\cdot\vec{dS} = \iiint_\Omega \rho \hspace{0.1cm}dV \\ \oiint_{\partial\Omega}\vec{B}(\omega)\cdot\vec{dS}=0 \\ \oint_{\partial \Gamma}\vec{E}(\omega)\cdot \vec{dl}=-j\omega\iint_{\Gamma}\vec{B}\cdot \vec{dS} \\ \oint_{\partial \Gamma} \vec{B}(\omega) \cdot \vec{dl} = \iint_\Gamma \vec{J}(\omega)\cdot\vec{dS} + j\omega\iint_\Gamma \vec{D}(\omega) \cdot \vec{dS}$$|$$ \nabla \cdot \vec{D}(\omega) = \rho \\ \nabla \cdot \vec{B}(\omega) = 0 \\ \nabla \times \vec{E}(\omega) = -j\omega\vec{B}(\omega) \\ \nabla \times \vec{H}(\omega) = \vec{J}(\omega) + j\omega\vec{D}(\omega)$$|


## Integral vs. Differential Forms:

Trying to find a solution for Maxwell's equations in the Integral form usually leads to a Problem requiring a Full-matrix solution. This means that most of the matrix elements are non-zero, and matter to the final answer.

On the other hand, when using the Differential form, solutions are most often found by solving a sparse-matrix Problem. This means that the Differential forms usually lead to matrices where most elements are null / zero.


### Why does this matter?
Solving full matrix Problems is much more expensive computationally. This makes it impractical to use integral forms for problems where the geometry - or the Problem's Spatial or Time Surface defining its boundaries - are too big, leading to a great amount of runtime.

A possible workaround this is to use Differential forms, leading to Sparse Matrices problems. The fact that most elements on a Sparse matrix are null means that dedicated methods to index and access only each non-null element of the matrix can be used, greatly increasing the speed of the algorithm while reducing the amount of memmory the Sparse-matrix occupies.