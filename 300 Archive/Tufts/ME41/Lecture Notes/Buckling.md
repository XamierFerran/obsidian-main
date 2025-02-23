#archive 
Compression of a structural member causes small axial deflection until a certain critical load causes significant bending (buckling) a.k.a. elastic instability

### Euler Equation
- Given a vertical column:
	- If force P is applied along centroidal axis, compression occurs for low force
	- When force reaches a critical value $P_{cr'}$ column becomes unstable and bending develops
- Euler column formula describes the critical value:
$$P_{cr}=\frac{C \pi^2EI}{l^2}$$
- $C$ is end conditon constant
- $E$ is modulus of elasticity
- $I$ is the second moment of inertia
- $l$ is initial length

Table 4-2: End-Condition constants
![[Pasted image 20221126174647.png]]

Fig. 4-18
![[Pasted image 20221126174717.png]]

- It is convinient to define slenderness ratio, $l/k$:
$$I = Ak^2$$
$$k=\sqrt{\frac{I}{A}}$$
- $k$ is radius of gyration
- $I$ is second moment of area
- $A$ is cross-sectional area

- $$\frac{P_{cr}}{A}=\frac{C\pi^2E}{(\frac{l}{k})^2}$$
Fig. 4-19
![[Pasted image 20221126185622.png]]
- $\frac{P_{cr}}{A} < S_y$ 
	- $\frac{P_{cr}}{A}$ cannot exceed yield strength $S_y$

### J. B. Johnson Equation
- Some slenderness rations, $\frac{l}{k}$ would not be suitable even if Euler equation suggests they are which is represented by the gray area.
- J.B. Johnson equation provides additional relationship/boundary
$$\frac{P_{cr}}{A}=S_y-(\frac{S_y}{2\pi}*\frac{l}{k})^2\frac{1}{C*E},\space\frac{l}{k}\leq(\frac{l}{k})_1 $$
Fig. 4-19
![[Pasted image 20221126191147.png]]

Table A-18
![[Pasted image 20221126191435.png]]

### Radius of Gyration and Slenderness
- Consider radius of gyration,$k = \sqrt{\frac{I}{A}},\space and \space slenderness \space ratio,\space \frac{l}{k}$
![[Pasted image 20221126192322.png]]
![[Pasted image 20221126192350.png]]


### Columns with Eccentric Loading
- Prior equations apply for ideal columns with force applied through centroidal axis
- Problems occur in which load eccentricities are unavoidable
- In addition to axial load, bending moments occur
- Eccentricity ratio (from given geometry) is defined:
$$\frac{e*c}{k^2}$$
- $e$ is eccentricity distance
- $c$ is distance from neutral plane to outer fiber (bending)
- $k$ is radius of gyration
![[Pasted image 20221126193541.png]]

Secant Column Formula:
$$\frac{P}{A}=\frac{S_{yc}}{1+(\frac{ec}{k^2}sec[(\frac{l}{2k})\sqrt{\frac{P}{AE}}}$$
Fig. 4-21
![[Pasted image 20221126193455.png]]