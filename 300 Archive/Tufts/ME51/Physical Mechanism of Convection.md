### Newton's Law of Cooling
![[Pasted image 20221130082534.png]]
![[Pasted image 20221130082553.png]]
![[Pasted image 20221130082625.png]]
- Shows that rate of convection heat transfer is proportional to the temperature difference
- Also shows us that the heat transfer coefficient **h** (according to the units in the equation) can be defined as the rate of heat transfer between a solid surface and a fluid per unit surface area per unit temperature difference
	- This relation is dope, but bc of its relation to so many variables it is still difficult to determine

Fluids traveling over a solid non-porous surface experiences no-slip condition

The flow region adjacent to the wall in which the viscous effects (and thus the velocity gradient) are significant is called the **Boundary Layer**

What causes both no-slip and boundary layer is viscocity

An implication of no slip is that heat transfer from the solid surface to the fluid later adjacent to the surfice is **pure conduction**
![[Pasted image 20221130101531.png]]
- T represents the temperature distribution
- $\frac{\delta T}{\delta y}_{y=0}$ is the temperature gradient at the surface
- Heat is then convected away from the surface as a result of fluid motion.

Using this equation and the equation further above we get
![[Pasted image 20221130101908.png]]
Really, this is the convection heat transfer coefficient when the temperature distribution is known. Notice, the only important terms in this are mostly just temperature variables.

h, the convection heat transfer coefficient, varies along the flow direction which is usually x. The average h for a surface is determined by averaging the local h's over the entire surface area $A_s$ or length $L$
![[Pasted image 20221130102524.png]]

### Nusselt Number
The nussellt number is a nondimensionalized form of the h.
![[Pasted image 20221130103126.png]]
- L is the characteristic length
- k is thermal conductivity

Physical reasoning of Nusselt Number
![[Pasted image 20221130103617.png]]
Really its a ratio between  convective and conductive heat transfer. The larger the nusselt number is, the more effective convection. A Nusselt number of Nu = 1 means the fluid layer being represented has heat transfer thats pure conduction.