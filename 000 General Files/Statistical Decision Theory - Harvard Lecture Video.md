---
tags:
  - areas/university/signal-detection
  - areas/statistical-decision-theory
---
Data sets are a thing, they are easier to interpret as graphs, they tend to come in a normal distribution shape but can also vary in distribution.

There are measures of middle values (mean, median mode)

There are measures of variability (range, variance, standard deviation)

Variability can be seen in normal distributions as how wide the base is

# Signal Detection Theory
Observed values of signals are usually normally distributed

However since they are observations of signals it is possible for the observation/graph to be affected (noise)

If you know the noise and the shape of both the actual data and the noise, it is possible to choose a threshold or criterion and create a rule (if it is above or below this it is this or not)

This means there are four options

![[Pasted image 20250311213020.png]]


When the observer says yes and it matches the signal (hit)

When the observer says yes and doesnt match the signal (false alarm)

Observer says no, matches with noise (correct rejection)

Observer says no and matches signal (misses)

The criterion mentioned above is formalized by this equation
![[Pasted image 20250311222400.png]]

d' is equal to the distance between signal and noise curve