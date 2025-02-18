*Block 4 p. 1 - 9*

**Heat Transfer** is the energy transferred from one body to another due to a temperature difference.

Heat Transfer = $\dot{Q}$ is a rate, energy transferred per unit time. It has units of Joules/sec = Watts 

There's lots of Q's ($\dot{Q'}\dot{Q''}\dot{Q'''}$)
- Each prime (apostrophe) relates to the number of length units (meters etc.) in the denominator
- ![[Pasted image 20221113233538.png]]

What's the difference between heat transfer and thermodynamics?
- Thermo is about amounts of energy generated via different proceses
- Heat transfer is all about rates

### Modes of Heat Transfer
- Conduction - Heat transfer in a medium due to atomic processes driven by a temp difference
	- ![[Pasted image 20221114000245.png]]
	- 1D Fourier Law of Conduction
		- $\dot{Q''_x}=-k\frac{dT}{dx}$
			- $\dot{Q''_x}=$ heat flux trasnfer rate per unit area
			- $-k=$ thermal conductivity (material property)
			- $\frac{dT}{dx}=$ temperature gradient
- Convection - heat transfer by bulk motion of fluid
	- Bulk motion of fluid is much more effective at transporting heat than random molecular motion
	- Usually we are interested in the heat transfer rate between a surface and a moving fluid at a different temperature
		- EX: ![[Pasted image 20221114001030.png]]
		- ![[Pasted image 20221114001056.png]]
		- Here, the heat transfer rate depends on the temperature gradient AT THE SURFACE. As you get farther away, the temperature gradient drops off until it is $T_{\infty}$. Notice this looks like a velocity boundary later in some ways--higher gradient closer to the surface, gradual decay towards far away conditions. 
		- Also notice this is basically just conduction right where the air meets the surface because U = 0 there.
			- However, once conduction transports heat away from the wall it is swept downstream. This means dT/dy = 0 is different than if you calculated only conduction in air.
- Forced Convection - motion of fluid is forced by something externally
	- EX: ![[Pasted image 20221117005725.png]]
- Natural Convection - Fluid still has bulk motion, but it is caused by temperature variations in chaning density
	- EX:![[Pasted image 20221117005830.png]]
- Convection heat transfer is often represented in terms of the convective heat transfer coefficient, h
	- $\dot{Q}=hA(T-T_{ref})$ or $h=\frac{\dot{Q}"}{(T-T_{ref})}$
	- Units: $[W]=[\frac{W}{m^2k}][m^2][K]$
	- Heat transfer is positive from the surface into the fluid. This is a consistent assumption.
	- $T_{ref}$ is representative of the fluid temperature. For external flow cases, $T_{ref}=T_{\infty}$
	- A simple example:
	- ![[Pasted image 20221117012808.png]]
- h Depends on a lot of things:
	- Geometry of object: cylinder, plate, rough, smooth, etc.
	- Fluid Properties: $k, C_p, \mu$
	- Size, flow speed
	- Reynolds numver
- h is useful because forced convection is linear. If you double $(T_s-T_{\infty})$, you will double $\dot{Q}$
- Radiation - heat transfer via photons
	- All objects continuously emit electromagnetic radiation. This is because of thermal motion causes electrons to get excited into higher energy states. As they fall back to equilibrium, they emit a photon. This is called thermal radiation. 
- Surface Energy Balance
	- All different heat transfer models, conduction, convection, radiation, can act in parallel or in series (like circuits)
	- EX: Roof of house