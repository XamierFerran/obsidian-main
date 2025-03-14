page 56/916 about 40 pages?

**Signal detection theory (SDT)** is a frame-work for understanding accuracy that makes the role of decision processes explicit.

![[Pasted image 20250312093808.png]]
**Detection** is when one of the possibilities of the stimulus is "null"
**Recognition** is when there is no "null" and you are discriminating on all variances of stimulus
![[Pasted image 20250312100129.png]]
# The Basic Experiment: One Stimulus Interval Per Trial
## Yes-No Design
- Simplest task that can be posed
- Four possible outcomes
$$H=hit\space rate=P("yes"|S)$$$$F=false-alarm \space rate=P("yes"|N)$$
## Normal-Distribution, Equal-Variance Representation
$$z(H)=M_S-c$$$$z(H)=M_N-c$$^d913e2
## Measures of Sensitivity and Response Bias
Sensitivity is not affected by the criterion but instead affected by the difference between the means of the distributions, which is denoted by d'
$$d'=M_s-M_N=z(H)-z(F)$$
Response bias is directly defined by the tendency to say yes or no which is defined by the location of the criterion. Its basically the person's personal belief. What they think is okay for all four categories.

An unbiased choice would be the halfway point between the distribution means. Moving the criterion left would create a more liberal "yes" response and right would be more conservative "no". A midpoint of 0 implies that $M_S=-M_N$ and c can be found in the below equation$$c=-\dfrac{1}{2}[z(H)+z(F)]$$
Early theorists said the strength (horizontal) axis is really a measure of likelihood, suggesting that c and $\beta$ the likelihood ratio are monotonically related
$$ln(\beta)=cd'$$
## How to calculate d' c, and $\beta$ 
In a low number of trial cases, it is possible to have case where H=1 or F=0. This would make z hard to calculate, so later theorists came up with a good approximation by adding or subtracting 0.5 to the frequency matrix when necessary. Examples below:
![[Pasted image 20250312110145.png]]
## Evaluating Sensitivity Measures: Receiver Operating Characteristic Curves
As the criterion moves from the right to the left along the decision access both H and F increase, that relationship is called the receiver operating characteristic (ROC).

Using this idea we can rewrite the equation on line [17](#^d913e2) of this document using this equation $$z(H)=d'+z(F)$$
which is a straight line with unit slope and intercept d'![[Pasted image 20250312111211.png]]
## Predicting Sensitivity and Bias Measures from Experimental Variables
