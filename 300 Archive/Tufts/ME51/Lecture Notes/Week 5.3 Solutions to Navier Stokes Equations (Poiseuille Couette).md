*Block 2, p.29-35*
#notdone 
**Background**
The Navier-Stokes equations are really hard to solve. So, we use specific situations that simplify the equations to solve them.

**Parallel Flow**
Assume:
- nonzero velocity in only one direction (x-direction)
	- v = 0 w = 0
	- steady ($\frac{\delta u}{\delta t}=0$)

Let's look at what happens to our equations when these assumptions are applied.

**Continuity Derivation** (conservation of mass for a differential control volume)
Before Assumptions
- $\frac{\delta u}{\delta x}+\frac{\delta v}{\delta y}+\frac{\delta w}{\delta z}=0$
After Assumptions
-  $\frac{\delta u}{\delta x}+0+0=0$
	- because we know v = 0 an w = 0
Therefore
- $\frac{\delta u}{\delta x}=0$
	- and u only depends on y and z variables

**X-Momentum Derivation**
Before Assumptions
- $\frac{\delta u}{\delta t}+u\frac{\delta u}{\delta x}+v\frac{\delta u}{\delta y}+w\frac{\delta u}{\delta z}=-\frac{1}{\rho}\frac{\delta P}{\delta x}+v(\frac{\delta^2 u}{\delta x^2}+\frac{\delta^2 u}{\delta y^2}+\frac{\delta^2 u}{\delta z^2})$
- First Term = 0 bc steady
- Second Term = 0 bc continuity equation
- Third Term = 0 bc v = 0 (assumption)
- Fourth Term = 0 bc w = 0 (assumption)
- First term in parenthesis is zero because it is second derivitive of constants
After Assumptions
- $-\frac{1}{\rho}\frac{\delta P}{\delta x}+v(\frac{\delta^2 u}{\delta y^2}+\frac{\delta^2 u}{\delta z^2})=0$
- Equation is linear so it can be solved which is great. The instance that it can be solved like this? 

**Couette Flow**
- Setup
	- Two infinite parallel plates with fluid between them 
	- ![[Pasted image 20221104133217.png]]
- Assumptions for simplification
	- steady
	- v=w=0
	- P=Patm (pressure gradient is zero)
	- $\frac{\delta u}{\delta z}=0$ -> u = u(y)
- The equation
	-  $-\frac{1}{\rho}\frac{\delta P}{\delta x}+v(\frac{\delta^2 u}{\delta y^2}+\frac{\delta^2 u}{\delta z^2})=0$
	- turns out we can simplify it more because of our specific assumptions
	- P = Patm so pressure term cancels out
	- $\frac{\delta u}{\delta z} = 0$ so $\frac{\delta^2 u}{\delta z^2} = 0$
- The final equation
	- $v\frac{\delta^2 u}{\delta z^2} = 0$ -> divide out the kinematic visc (just a constant)
	- $\frac{d^2 u}{d z^2} = 0$
	- Now we can just integrate with boundary conditions
- Boundary Conditions
	- No-Slip occurs, so
		- u(-h) = 0
		- u(h) = U
- General Solution
	- $u = C_1y + C_2$
- Apply BC
	- ![[Pasted image 20221104134229.png]]
		- Video error, constanst are switched

- In questions, sometimes they'll ask for shear stress
	- $\tau_{xy}=\mu\frac{\delta u}{\delta y}=\mu\frac{U}{2h}=$ constant throughout flow 
		- Above equation represents x direction stress applied on y direction faces
		- ![[Pasted image 20221104134754.png]]
		- note: since u only varies in the y-direction the above calculation for shear stress is sufficient but we'd have to do more if it were in more directions. 

**Poiseuille Flow**
