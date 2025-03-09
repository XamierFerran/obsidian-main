#archive 
*Block 2, p.36-39*

**Background**
Similar to Poiseuille flow but in a tube instead of infinite parallel plates.

Setup
- ![[Pasted image 20221104143245.png]]
- Fully developed
	- $\frac{\delta x}{\delta x} = 0$, u = u(r)

We are looking for the velocity as a function of r and x. But, it won't vary as a function of x because it is fully developed.

Now, we could derive the N-S equations in cylindrical coordinates, but Erica just gave us the equation which is nice. 

$u(r)=\frac{1}{4\mu}(-\frac{dP}{dx})(R^2 - r^2)$

This looks like a parabaloid function, so

![[Pasted image 20221104161819.png]]

If we look at the graph we see that **max velocity** is $$u(0) = u_{max} = \frac{R^2}{4\mu}(-\frac{dP}{dx})$$
What is volume flow rate?$$Q=\int_{0}^{R}{u(r)(2\pi rdr)}=\frac{\pi R^4}{8\mu}(-\frac{dP}{dx})$$
![[Pasted image 20221104164524.png]] Differential slice of area

What is average velocity?$$u_{avg}=\frac{Q}{A}=\frac{Q}{\pi R^2}=\frac{R^2}{8\mu}(-\frac{dP}{dx})$$This equation is subtly pretty dope because it relates our pressure gradient to our tube size for a fixed flow rate.
$$\frac{dP}{dx}=-\frac{8\mu Q}{\pi R^4}$$
Notice that the radius is under and to the fourth power. That's a HUGE dependancy. We can use this to calculate pressure gradient with a finite length of tube and a finite radius