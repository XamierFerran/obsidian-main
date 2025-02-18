**Xamier Ferran**
**ME193**
## For HW03, design a pedometer based on accelerometer measurements. Create and implement a decision rule to identify each step and a counter for the number of steps. You can test your algorithm by counting your steps as you walk a straight path to see how well your algorithm works. 
## Write a short report, preferably in bullet form, not much longer than a page, to describe your experiment.
![[Pasted image 20250213213820.png]]
### Data Interpretation
- Placing the phone on a flat surface revealed the direction of earth's gravity. By orienting the phone in different positions, I was able to determine that in the phone's vertical position gravity is in the negative y direction. This means that the x and z directions are valued at zero as there is no gravitational acceleration in that direction.
- Using this information, I can detect the beginning and end of each step when the x and z accelerations reach zero as that is when my foot is stationary.
- To capture this motion, I taped my phone specifically to my toe because that stays at a stationary position for the longest amount of time.
- Given the attached data and above graph, the algorithm correctly determined 6 steps
### Decision Rule:
- A step is determined as the motion between each near zero acceleration point in a graph of vertical acceleration versus time
- At a time point where the acceleration is near zero (or stabilized), that would be the beginning of the current step and end of the last step
- In other words, this stabilized acceleration value represents there being no significant acceleration in plane with the floor. If my foot were moving forward or sliding around, this would no longer be true
- The algorithm works as follows:
	- extract time data and acceleration in the y direction (since that one is closest to zero)
	- This data is then smoothed over to filter out noise
	- Peaks are detected to differentiate from the stabilized portions
	- The program steps through each time step, and detects when a local maxima occurs. 
	- It then checks for the stabilized region to consider the step completed