---
tags:
  - areas/university/information-theory
  - areas/university/human-machine-system-design/discussion-post-reading
  - areas/university/human-computer-interaction
author: Wanyu Liu, Antti Oulasvirta, Olivier Rioul, Michel Beaudoin-Lafon, Yves Guiard
year published: "2019"
---
## Information Theory Concepts

![[Pasted image 20250309172322.png]]

It states that a source produces messages, modeled as a random variable X , which are adapted by an encoder and then sent over a channel and decoded by a decoder to the final destination. The input of the channel is X and the output of the channel to the receiver is Y . Since there might be noise in the channel, output Y does not always equal input X . The engineering process to transmit a source message X through the channel does not concern the semantic aspect of communication, but is only related to the probability of each possible outcome. Therefore, the channel is completely described by the probability $p(Y|X)$ of Y given X .

## Information-Theoretic Applications in HCI

### What is Throughput in Fitt's Law?

Fitts conceptualized the human motor system as a communication channel and proposed an operationalized formula to capture the relationship between movement time MIT and what we call index of difficulty ID. Fits also derived the Index of Performance IP, which is computed by dividing ID by the empirically determined movement time $MT: \dfrac{ID}{MT}$ , to represent the participant's maximum rate. This notion was later borrowed as "throughput", which in engineering is widely used to measure an effective speed of data transmission.

### How Relevant is Hick's Law for HCI

There is debate of its usefulness in HCI, but it is more commonly used in the design community. According to the author's findings it is not very relevant.

### A Human-Computer Communication Framework

![[Pasted image 20250309174329.png]]
