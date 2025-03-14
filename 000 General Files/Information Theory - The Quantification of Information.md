---
tags:
  - areas/university/information-theory
  - areas/university/human-machine-system-design
  - areas/university/human-machine-system-design/discussion-post-reading
author: Christopher D. Wickens, Justin G. Hollands
year published:
---
**Information** is defined as the reduction of uncertainty
**Information Theory** formally quantifies the amount of information conveyed by a statement, stimulus, or event. The quantification is influenced by three variables:
1. The **number of possible** events that could occur, N
2. The **probabilities** of those events
3. The **events' sequential constraints**, or the context in which they occur
## Number of Events
Before the occurrence of an event a person has a state of knowledge that is characterized by uncertainty about some aspect of the world. After that event, that uncertainty is normally less. The amount of uncertainty is reduced by the event is defined by the average minimum number of true-false questions that would have to ve asked to reduce the uncertainty.$$H_s = log_2 N$$
where $H_s$ is an event, and N is the number of equally likely alternatives.

## Probability
The amount of information conveyed also depends on frequency or likelihood. Thus, the probabilistic element of information is quantified by making rare events convey more bits.$$H_s=log_2 \dfrac{1}{P_i}$$
where $P_i$ is the probability of occurrence of event i

Often, psychologists are more interested in measuring the average information conveyed by a series  of events with differing probabilities. To measure the average we use this equation:$$H_{ave}=\sum_{i=1}^{n}P_i[log_2(\frac{1}{P_i})]$$
