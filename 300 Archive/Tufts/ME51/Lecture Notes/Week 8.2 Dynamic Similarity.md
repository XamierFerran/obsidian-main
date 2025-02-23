#archive 
Block 3, pg. 38-43

In the first video for this week (Week 8.1), we talked about how to non-dimensional the Navier-Stokes equation and what it means to have non-dimensionalized equations. 

**Let's See How to Actually Use This**
- Example: We are tasked with taking pressure measurments around an airplane flying in the air with some parameters.
	- $u_{\infty} = 150 \frac{m}{s}$
	- $L = 50 m$
	- $v = 1.5x10^-5 \frac{m}{s}  @  20 C$
	- $Re = \frac{LU_{\infty}}{v}=5*10^8$
	- Evidently, you can't just stick an airplane in a lab. So we scale down
	- We are going to model air using water!
		- We need to match the Re 
		- $Re_{air}=Re_{water}={\mu}5*10^8=\frac{L_{\mu}u_{\mu}}{v_{water}}$
		- $v_{water}=10^{-6}\frac{m^2}{s}$
		- $L_{\mu}u_{\mu}=500(\frac{m^2}{s})\rightarrow$ maybe $u_{\mu}=25(\frac{m}{s}),L=20m$
			- These numbers are really us just coming up with reasonable numbers that we can use for experiments while also making sure they still fit into the equation.
	- Now let's measure the pressure from the experiement
		- Will this give us the correct pressure?
		- No!
		- It will give us the dimensionless pressure
		- So, for an airplane we expect it's pressure to be inertia dominated
			- $P^*=\frac{P-P_{\infty}}{\rho U^2_{\infty}}$
			- So long as our dimentionless setup is the same, P* should be correct
			- To get the actual pressure from the pressure we get from the model
			- Well, it turns out that we can reverse the process
				- $P^*_{M}=P^*_{A}$
					- M = Model, A = Actual
				- $\frac{P_M-P_{\infty,M}}{\rho_M U^2_{\infty,M}}=\frac{P_A-P_{\infty,A}}{\rho_A U^2_{\infty,A}}$
			- In the experiment you'd measure for $P_M-P_{\infty,M}$. The denominators are known generally. That means you can solve for $P_A-P_{\infty,A}$

This is all highly applicable, but Re isn't the only number that can be non-dimensionalized to find dynamic similarity. There are many others! check in Block 3 Page 42 of the reading notes there are examples. To figure out which to use, write out the form of Navier Stokes equations that describes the problem your tackling and the boundary conditions. 
- From Lecture Notes: "How do you know which dimensionless parameters are important to  
your specific problem? Write out the form of the Navier-Stokes  
equations that describe your problem and the boundary conditions, then  
follow the nondimensionalization procedure we described above. When  
each term in your equation is unitless, you will have coefficients that  
together make nondimensional numbers. You have to match ALL of  
them in your model if your model is going to reproduce the flow  
correctly! Don’t worry about knowing the names of the parameters you  
are matching. If you match what you see in your equation and boundary  
conditions, you will get the right answer"