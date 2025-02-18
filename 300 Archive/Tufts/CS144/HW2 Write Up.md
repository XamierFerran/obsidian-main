# HW2: Particle Filter
###### Tufts University
###### CS141 Probabilistic Robotics
###### by Xamier Ferran
## 1 Overview
$\quad$The objective of this homework assignment is to implement a particle filter program focused on drone localization. The associated program visualizes the particle filter algorithm as the drone moves through each time step. At each sequential time step, the particles adjust to approximate the drone's location more accurately by utilizing the noisy observation images provided by the drone. Over time, a cluster of particles forms around the area where the drone is located, enabling effective localization. 
$\quad$The program generates bar graphs that plot cluster probabilities and average distances across the time steps for further analysis. These graphs indicate that the cluster probability consistently reaches a high point, while the average distance tends to stabilize at a low point over ten time steps, regardless of the observation dimensions set at $5$, $10$, or $20$ units.
## 2 Simulation Environment 
$\quad$The simulation environment is the defined space where drone mobilization and measurements are taken. It is defined by an RGB image of fixed dimensions with its origin at $(0,0)$, which is the center of the image. Within this environment, one unit of space is defined by 50 pixels.
### 2.1 Drone Measurement
$\quad$At the beginning of each simulation, the drone's starting position $(x,y)$ is defined somewhere within the bounds of the image and randomly determined by a uniform distribution that maps across the image. At each time step, the drone captures a noisy sensor reading of size $m \times m$  where $m$ is defined as 50 units of distance. A range of $m$ sizes were tested to determine how it would affect localization, 50 units seem to be fine.
### 2.2 Drone Movement
$\quad$At each time step, the drone's movement is defined as a vector limited in magnitude by the equation $$dx^2 + dy^2 = 1.0$$where $dx$ and $dy$ are defined as small changes in $x$ and $y$ respectively. Sensor noise $\in[0,\sigma]$ is added to $dx$ and $dy$ for realistic sensor representation. The direction is determined by a random angle $\theta$ within $[0,2\pi]$. The overall equation for each consecutive drone position is: $$x_{new} = x_{old} + dx_{noisy}$$$$y_{new} = y_{old} + dy_{noisy}$$
$\quad$These definitions keep the drone from jumping around the map in an unrealistic way while remaining random. Any resulting movement vectors that lead the drone to move outside the image area are rejected and recalculated until the final movement vector is within the space. 
$\quad$Finally, the drone's true position is denoted to the user as a red dot. Running the program code at this point allows the drone to move randomly across the map reporting a noisy image at each time step. 
## 3 Particle Filter Implementation 
$\quad$ The particle filter algorithm works to efficiently identify the drones location by distributing particles across the map and comparing the observation of each particle to that of the drone. Each time step providing a better estimation for the drone's location.
### 3.1 Particle Initialization
$\quad$ Implementation of the particle filter within the simulation environment begins with the initialization of uniformly distributed particles across the image on the first step. In the following steps, a series of calculations take place to compute necessary information for filtering. 
### 3.2 Comparison & Resampling
$\quad$ At each time step, the particles are compared to the observation image provided by the drone. The particles closest to the observation image are given a higher weight, which will enforce greater influence over the positioning of the particles in the next time step. Resampling occurs at each time step, and the total number of visible particles decreases as the particles cluster around the drone. Using the movement vector used to move the drone, the particles are influenced by that as well as sensor noise.
### 3.3 Program Demo
$\quad$ Below is a series of figures taken from the system environment as the program is running after including the particle filter algorithm. For brevity and relevance, only a subset of images are included, as incorporating all images would be redundant.
![[timestep0.png|desc]] Figure 1 - Time Step 0
![[timestep5.png|desc]] Figure 2 - Time Step 5
![[timestep10.png|desc]] Figure 3 - Time Step 10
![[timestep15.png|desc]] Figure 4 - Time Step 15
![[timestep20.png|desc]] Figure 5 - Time Step 20
## 4 Experiments
$\quad$To evaluate the effectiveness of the particle filter within the simulation environment, performance was compared over multiple trials as the observation image dimensions increased in size. Varying the observation image dimensions provided insight into how the simulation performed given a greater or lesser amount of information per time step. To aid in this analysis, two metrics were collected:
- **Cluster Probability:** The likelihood that the particle filter successfully concentrates a majority of particles within a specified radius around the true position. This metric indicates how effectively the filter narrows down the probable region of the target.
- **Average Distance to True Position:** The mean Euclidean distance between the true position and the weighted average of particle positions. This metric provides a quantitative measure of the particle filter's accuracy in estimating the true position.
For each dimension, three trials were conducted to emphasize reproducibility.
### 4.1 Graphs
![[clusterM5T1.png|desc]] Figure 6 - Trial #1
![[clusterM5T2.png|desc]] Figure 7 - Trial #2
![[clusterM5T3.png|desc]]Figure 8 - Trial #3
![[avgM5T1.png|desc]]Figure 9 - Trial #1
![[avgM5T2.png|desc]]Figure 10 - Trial #2
![[avgM5T3.png|desc]]Figure 11 - Trial #3
![[clusterM10T1.png|desc]]Figure 12 - Trial #1
![[clusterM10T2.png|desc]]Figure 13 - Trial #2
![[clusterM10T3.png|desc]]Figure 14 - Trial #3
![[avgM10T1.png|desc]]Figure 15 - Trial #1
![[avgM10T2.png|desc]]Figure 16 - Trial #2
![[avgM10T3.png|desc]]Figure 17 - Trial #3
![[clusterM20T1.png|desc]]Figure 18 - Trial #1
![[clusterM20T2.png|desc]]Figure 19 - Trial #2
![[clusterM20T3.png|desc]]Figure 20 - Trial #3
![[avgM20T1.png|desc]]Figure 21 - Trial #1
![[avgM20T2.png|desc]]Figure 22 - Trial #2
![[avgM20T3.png|desc]]Figure 23 - Trial #3
## Discussion
$\quad$The average distance to true position remained relatively stable after 10 time steps across all observation sizes and trials. The average distance converges between 2 and 4 units, but more specifically hoovers around 3 units. It's also worth noting that the starting average distance tends to range from 8 to 12 units with a bias towards 8 units. 
$\quad$Cluster probability consistently seems to have a local peak between time step 4 and 10 with a global peak at the final time step. It is evident that cluster probability trended upwards as time progressed within the simulation. Across observation sizes, the graphs followed the same trends with hardly any difference between each other. 
$\quad$The variation of observation dimensions in size did not seem to significantly affect the particle filters overall performance. It is possible that greater variance and number of trials could provide higher resolution for data analysis.