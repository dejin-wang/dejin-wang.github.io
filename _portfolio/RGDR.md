---
title: "Reward-Guided Domain Randomization (RGDR)"
excerpt: "A project proposing an adaptive domain-randomization framework that improves robustness and generalization of autonomous-driving RL policies through reward-guided sampling.<br/><img src='/images/RGDR.png' style='width:200px;'><br/><a class='btn btn--primary' href='https://github.com/dejin-wang/reward_guided_domain_randomization' target='_blank'>View Code on GitHub</a>"
collection: portfolio
---


## Project Overview
This project introduces **Reward-Guided Domain Randomization (RGDR)**, a scalable and principled framework designed to improve the robustness and zero-shot generalization of reinforcement-learning policies for autonomous driving. Unlike traditional domain randomization that samples parameters uniformly, RGDR adaptively prioritizes challenging environments using real-time reward feedback, enabling policies to focus on scenarios where they currently underperform.

## Key Contributions
- **Reward-Based Training Metric:** Introduced mean reward per step as a stable and algorithm-agnostic indicator of environment difficulty, applicable to both value-based and policy-gradient RL methods.
- **Adaptive Sampling Strategy:** Developed a reward-guided weighted KDE method that assigns higher sampling probability to low-reward environments, emphasizing difficult regions of the domain space.
- **Efficient Exploration–Exploitation Balance:** Designed a dynamic sampling mechanism that transitions from broad exploration to targeted exploitation without additional network components.
- **High Computational Efficiency:** Achieves linear or sublinear complexity per iteration, significantly lower than Active Domain Randomization (ADR), while maintaining similar or superior robustness.

## Technical Highlights
- Weighted Kernel Density Estimation (KDE) for difficulty-aware environment sampling  
- Linear-complexity sampling pipeline with constant-time perturbation and buffer updates  
- Integration with PPO for large-scale autonomous-driving tasks  
- Extensive evaluations in both OpenAI Gym (Pendulum-v1) and CARLA (Adaptive Cruise Control)

## Experimental Results
- **OpenAI Gym:** RGDR emphasizes harder gravity intervals, improving robustness without excessive sampling. It outperforms uniform DR in difficult scenarios and achieves performance comparable to ADR with far lower computation cost.
- **CARLA Autonomous Driving:**  
  - Demonstrated strong generalization across randomized road friction and vehicle mass settings.  
  - Achieved higher rewards in challenging and out-of-distribution conditions relative to UDR and ADR.  
  - Validated that adaptive sampling leads to more balanced and effective policy training.

## Outcome
RGDR provides a general, scalable, and computationally efficient solution for training robust autonomous-driving RL policies. The method outperforms or matches state-of-the-art baselines while reducing computational overhead, making it suitable for high-dimensional, safety-critical driving tasks such as those simulated in CARLA.  
This project forms the basis of ongoing work on robustness, sim-to-real transfer, and domain adaptation in autonomous driving.
