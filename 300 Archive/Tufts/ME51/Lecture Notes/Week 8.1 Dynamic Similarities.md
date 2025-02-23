#archive 
Lecture Block 3, p.33-38

### Principal of Dynamic Similarities:
If one removes the units from the Navier-Stokes equations and the bondary conditions for a particular flow its possible to find a single flow solution that works for a large class of flows.

### Example: Let's say we have a blob...

![[Pasted image 20221031201930.png]]

The goal is to make all of the variables, including boundary conditions, non-dimensional in terms of appropriate scales of the problem 

**Non-Dimensional Variables** should vary from about 0 to about 1 or 1 to -1

Non-Dim Velocity = u*
$u* = \frac{u}{U_{infinity}}$
	Basically this means that u is the varying variable. It can represent flow velocity close to the surface or forever away. At close to the surface there is no slip so it is at zero. Far from the surface $u = U_{infinity}$ so the fraction representing u* equals 1. 

Non-Dim Position = x*
$x* = \frac{x}{L}$ 
	Similar to Non-Dim Velocity

Non-Dim Time = t*
$t* = \frac{tU_{infinity}}{L}$
	Similar to Non-Dim Velocity

Non-Dim Pressure is a special case because it depends
	Inertia/Momentum Dominated Pressure = P* (For High Re)
	$P* = \frac{P-P_{infinity}}{\rho U_{infinity}^2}$
		The numerator is pressure and the denominator is inertia/momentum flux
	Viscous Force Dominated Pressure  = P* (For Low Re)
	$P* = \frac{(P-P_{infinity})L}{\mu U_{infinity}}$
		The numerator (except L) is a measure of pressure and the denominator (plus L on the numerator) is a measure of viscous force.
	