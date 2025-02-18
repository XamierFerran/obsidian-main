<center><h1>HW2: Particle Filter</h1></center>
<center><p>Tufts University</center>
<center><p>CS141 Probabilistic Robotics</center>
<center><p>by Xamier Ferran</center>
<h2> 1 Overview </h2>
<p>The objective of this homework assignment is to implement a particle filter program focused on drone localization. The associated program visualizes the particle filter algorithm as the drone moves through each time step. At each sequential time step, the particles adjust to approximate the drone's location more accurately by utilizing the noisy observation images provided by the drone. Over time, a cluster of particles forms around the area where the drone is located, enabling effective localization. 
$\quad$The program generates bar graphs that plot cluster probabilities and average distances across the time steps for further analysis. These graphs indicate that the cluster probability consistently reaches a high point, while the average distance tends to stabilize at a low point over ten time steps, regardless of the observation dimensions set at 5, 10, or 20 units.</p>
<h2>2 Simulation Environment </h2>
$\quad$The simulation environment is the defined space where drone mobilization and measurements are taken. It is defined by an RGB image of fixed dimensions with its origin at $(0,0)$, which is the center of the image. Within this environment, one unit of space is defined by 50 pixels.
<h3>2.1 Drone Measurement</h2>
$\quad$At the beginning of each simulation, the drone's starting position $(x,y)$ is defined somewhere within the bounds of the image and randomly determined by a uniform distribution that maps across the image. At each time step, the drone captures a noisy sensor reading of size $m \times m$  where $m$ is defined as 50 units of distance. A range of $m$ sizes were tested to determine how it would affect localization, 50 units seem to be fine.
<h3>2.2 Drone Movement</h3>
$\quad$At each time step, the drone's movement is defined as a vector limited in magnitude by the equation $$dx^2 + dy^2 = 1.0$$where $dx$ and $dy$ are defined as small changes in $x$ and $y$ respectively. Sensor noise $\in[0,\sigma]$ is added to $dx$ and $dy$ for realistic sensor representation. The direction is determined by a random angle $\theta$ within $[0,2\pi]$. The overall equation for each consecutive drone position is: $$x_{new} = x_{old} + dx_{noisy}$$$$y_{new} = y_{old} + dy_{noisy}$$
$\quad$These definitions keep the drone from jumping around the map in an unrealistic way while remaining random. Any resulting movement vectors that lead the drone to move outside the image area are rejected and recalculated until the final movement vector is within the space. 
$\quad$Finally, the drone's true position is denoted to the user as a red dot. 
<h2>Experiments</h2>
<h2>Evaluation</h2>
<h2>Results</h2>
<h2>Discussion</h2>
