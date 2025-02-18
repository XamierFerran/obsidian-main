#discussion-post-reading #introduction-to-shared-control #shared-control
by Mishel Johns

## Abstract
This paper focuses on the tacit expectations involved in a shared control automated system. Through the experimental study, the researchers learned that the driver tends to respond well to simple trajectory intentions communicated by the automated system, but didn't handle more complex signals as well. This is primarily due to the fact that the automated system can only provide feedback through the steering wheel, and the driver tends to interpret jerky feedback as an automation system failure.
## Introduction
Different degrees of autonomous driving provide different benefits. Some of the main benefits of shared control is that it facilitates a gradual shift towards autonomous driving that keeps the user aware and in the loop.
## Background
Application being tested is called haptic feedback, where the steering wheel takes in the input of the driver and the automated system sends a gentle torque signal to the steering wheel that the user could easily override or correct.
### Vehicle automation and shared control
Shared control implementation:
1. Input mixing shared control (user + autonomous system)
2. Haptic feedback
Shared control might also be helpful in transitioning between fully manual control to fully autonomous control. One proven strategy is gradually increasing the level of haptic feedback involved.
### Challenges in shared control
**Adaptation force**: When users become used to haptic feedback, their force input adapts. This means there is greater error when there is no haptic feedback. This is a consideration to keep in mind in the case where autonomous systems don't work.
**Appropriate level of trust**: Users become complacent and over reliant.
**Intuiting driver plan**: Conflicting intentions between system and driver despite wanting to reach the same end goal.
**Communicating vehicle state**: Basically let the driver know what the autonomous system is intending to allow the driver to catch any errors
**Understanding driver responsibility in critical situations**: How do drivers react to situations where the system gives them full control
### Communicating through haptics
There is much literature regarding how humans feel about communicating through haptics and how the psychology differs between when the human driver knows its a robot vs them thinking its a human.
### HRI and socially sourcing interaction
Humans have a social model for any technology they interact with
## System
### Driving simulator
Cool Stanford driving simulator with lots of sensors. Secondary driver (representing the autonomous system) has a lamer setup. The secondary driver can input haptic feedback, and the driver that sends a larger input in steering wheel, brake, and throttle will hold the control.
## Methods
### Participants and Procedure
Driver not told about the human secondary driver. However the "driver agent" was briefed of their role and given short training on the system without the knowledge of the driver to avoid issues of trust. The driver is told that an automated system is helping them.
### Driving Course and Events
25 mile driving simulator. Based on likely failure scenarios of automation at level II and III. Events include a false positive (agent thinks there is a reason to act but not really), a false negative (the agent doesn't detect forcing the driver to respond), and a true positive (where the agent sees the conflict and correctly brakes)
![[Pasted image 20250210185131.png]]
## Results
### Communication
Moving the steering wheel slightly was good to communicate lane changes, but not great for more nuanced ideas since the wheel is both the indicator and the actuator of motion.
Driver and agents suggested another sensory input would be useful for communication such as turn signals. Some suggested that the next generation of autonomous vehicles should be socially interactive. A simple communicative "hi" was enough to make some drivers think the car was intelligent enough to be worth trusting.
### Communication Availability
