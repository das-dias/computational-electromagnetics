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

## Aditional Relations

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
