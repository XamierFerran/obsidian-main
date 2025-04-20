---
tags:
  - areas/university/ethics-in-ai
  - areas/university/generative-ai
  - areas/university/visual-language-action-models
author: Borong Zhang, Yuhao Zhang, Jiaming Ji, Josef Dai, Yuanpei Chen, Yaodong Yang
year published:
---
### Introduction / Lit Review
Vision language models expand on large language models by understanding both text and images allowing them to follow multiple modes of instruction. 

Vision language action models take it a step further allowing robots to follow vision language instructions and perform task in real world environments. 

As VLAs continue to evolve, they have the potential to become general policies for all robots to align them with human values.

%%
This is a large claim to make without more information on how vla could lead to general policies or if general policies would be a good idea to invest.
%%

Papers describe safety risks in LLMs and VLMs
- misleading content
- producing discriminatory statements
- facilitating criminal activities
- amplifying biases

Papers working to ensure safety by proposing
- data augmentation
- content moderation
- RL from human feedback
- light weight alignment

Further safety concerns
- physical risks
	- potential harm to the environment
	- hardware
	- humans
	- mental affects in near by humans
	- avoid changing the state of unrelated objects
- example: when a robot performs a task in a room
	- must not damage the environment or itself
	- change the state of unrelated objects
	- when interact with humans, robot should limit its speed and torque to avoid rushing task (offense or distress)

Challenge being addressed
Despite large-scale multitask behavior cloning and careful alignment in existing
VLAs even the most advanced models have yet to explicitly define and integrate
safety as an integral aspect of their design. This fundamental limitation introduces safety flaws within the model itself, limiting the deployment of VLAs in real-world applications.

%% Supposedly learns while being deployed according to bottom of page 2, but not listed in the contributions. Learning limited to training?%%

Contributions
- We introduce Safety-CHORES, a new simulation benchmark with millions of unique scenes that incorporate safety constraints. The diversity of these scenes ensures that the safety constraints introduced during training are scalable and generalizable, while also enabling a comprehensive evaluation of model safety. Our qualitative and quantitative analyses expose inherent shortcomings in current VLAs: their failure to integrate safety considerations explicitly.
- We propose the SafeVLA framework, which directly addresses the critical limitation of existing VLAs by incorporating explicit safety modeling through a constrained learning paradigm.
- We demonstrate through a series of experiments: from simple to complex tasks, that SafeVLA achieves state-of-the-art results in both safety and task performance. The performance and safety gains of our approach generalize across 12 distinct OOD task combinations, derived from 4 perturbations and 3 tasks, across over 500 procedurally generated scenes.
- We will open-source our code, data, models, and the newly proposed benchmark environment to facilitate further research in this area.

### Related Work
**Vision-Language-Action Models**, which predict robot actins, have made rapid progress due to breakthroughs in computer vision and natural language processing

VLA trained before hand and generalized to unseen settings

Existing research focused on expanding training scale and model size using existing VLMSs as the backbone, this paper uses SPOC

SPOC is a transformer-based model pre-trained on millions of frames of expert trajectories.

**Safety Alignment** 
Foundation models pre-trained on massive datasets have already demonstrated their remarkable capabilities and versatility. However, outputs if these models sometimes lead to unforseen negative consequences such as
- assisting criminal activities
- generating misinformation
- amplifying biases
- producing harmful content
Which is why alignment is important

Proor work depicts methods of aligning foundation models with safety objectives

RLHF based methods aligjn models with binary human preferences but struggle with complex trade-offs
%%no durrrrr%%

Safe-RLHF further refines by optimizing to ensure safety constraints are prioritized

Prior work shows fine tuning VLAs for alignment using reinforcement learning to improve generalization ability and performance rather than directly aligning with human intentions and values
%%RL instead of hardcoding values....hmm%%

This paper starts with pretrained model and then uses RL to align he model with task objectives

### Problem Formulation
whole lotta math

### Method: SafeVLA
Reference image
#### Information from figure 1
Three typical unsafe behaviors of the standard VLA during grasping
1. severe damage to irrelevant objects
2. misidentification of the target leading to the abuse of hazardous objects
3. interaction with dangerous objects while executing the instruction

**Bottom Left:** An example of navigation route showing three typical unsafe behaviors
- bang the handle
- circle aimlessly
- ram the frame
**Middle:** A comparison between SafeVLA and the standard VLA, SafeVLA balances safety and task performance 
%%I'd argue safety should be top priority, but I guess it'd struggle to complete if it is constantly stopped by safety concerns. There has to be a balance%%
**Right:**

To address challenges presented above, specify two constraints:
1. Object Safety Constraint
2. Robot Safety Constraint

### Safety Constraints
%%Using a simulation to train and tweak their data but the original problem is the unpredictability of real world robot interaction%%

### Experiments
**Questions to address:**
- What benefits arise from decoupling safety and task performance objectives in SafeVLA? (Section 5.2.1)
- Does SafeVLA balance safety and task performance efficiently? (Section 5.2.2)
- Can SafeVLA generalize to out-of-distribution (OOD) perturbations? (Section 5.2.2)

#### Experiment Setup
- AI2THOR simulator
	- 150k houses generated
	- 800k 3d object assets annotated
- Safety-ObjNav tasks, the robot must navigate through multiple rooms to find a designated object
- Safety-PickUp tasks start with the robot in a fixed position, instructing it tto pickup a specific object using its arm and gripper
- Safety-Fetch tasks combine both challenges, requiring the robot to first navigate across multiple rooms to locate the target object and then pick it up
	- For all tasks natural language instructions are provided and the robot;s observations consist solely of RGB images captured from two egocentric cameras positioned at different angles for nav and manipulation
- %% Check out appendix c for more info on experimental setup, worth checking out the paper on SPOC since that is the entire basis for their model. What changes did they make to SPOC that turned it from VLA to SafeVLA%%
- **Evaluation Metrics**
	- Cumulative object cost
	- Cumulative robot costs
# Arguments
- Overstating themselves. Should've said solving problems in a robotic simulation, I do not think this would hold up to the scrutiny and unpredictability of a real world robotic trial. Something to work on in the future would actually be having a test bed to implement this since the software seems to already be there.
	- This becomes more evident when looking at the ood perturbations in Table 2 where SafeVLA varies per task and sensory distrurbance
	- ^This table would be more useful if it also compared the previous software's compared in table 1 to give some context to the variation.
	- Wear overtime of components and how that would cascade over its performance
- Minimal safety for humans, seems to just be slowing down to avoid scaring a human not even to necessarily keep them safe. evaluation metrics fully disregard human interaction
	- This can probably be generalized into lack of human-robot interaction study. Why didn't then try running an experiment to actually see how humans react to robots etc. they didn't even seem to cite a paper referencing this and this is a well studied field
	- slowing down robot movement is a well studied field in automation, why is this not touched on in this context.