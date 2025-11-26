---
title: "Robust Reinforcement Learning for Autonomous Driving in Uncertain Environments"
excerpt: "A history-dependent reinforcement-learning framework that improves policy adaptability and robustness in dynamic, partially observable driving environments using randomized dynamics, context-aware rewards, and LSTM-based policy optimization.<br/><img src='/images/Robust_1.png' style='width:200px; max-height:180px; object-fit:contain;'><br/>"
collection: portfolio
---



## Project Overview
This project presents a **history-dependent reinforcement learning framework** designed to improve the robustness and adaptability of autonomous driving policies operating in dynamic and uncertain environments. Conventional RL methods assume fixed transition dynamics, static reward structures, and Markovian state representations, making them prone to overfitting and brittle behavior under real-world disturbances such as varying road friction, weather conditions, and unpredictable traffic interactions.  
To address these limitations, the proposed framework integrates **randomized training dynamics**, **context-aware reward functions**, and **LSTM-based PPO policies** that learn from historical interactions. This enables the agent to infer latent environmental variations implicitly and adjust its driving strategy in real time without requiring explicit access to environment parameters.

## Key Contributions
- **Randomized Training Dynamics:** Introduces structured variations in environmental parameters (e.g., friction, weather) during training, improving robustness to a wide range of driving conditions.
- **Context-Aware Reward Functions:** Dynamically adjusts the importance of safety, efficiency, and comfort objectives based on sampled environment conditions, enabling scenario-specific behavior.
- **LSTM-Based PPO Policy:** Utilizes an LSTM-augmented policy to capture temporal dependencies and infer hidden environmental factors from history, enabling adaptive behavior in non-stationary settings.
- **Fine-Tuning–Free Deployment:** Achieves environment-aware adaptation without requiring online task identification or real-time parameter estimation.

## Technical Highlights
- History-dependent formulation with LSTM to overcome partial observability  
- Environment-parameterized transitions and adaptive reward scaling  
- PPO optimization with stable surrogate objectives and entropy regularization  
- Evaluation across rainy, normal, high-friction, and randomized conditions in CARLA  
- Comparative analysis against domain-randomization and fixed-environment baselines  

## Experimental Results
- **Convergence Analysis:** The LSTM-based PPO agent shows stable convergence, with decreasing total loss and rising accumulated reward across training.
- **Generalization Across Environments:**  
  - Achieves near–state-of-the-art performance across rainy, normal, and high-friction conditions.  
  - Consistently ranks second-best or best in every fixed environment despite not being trained specifically for any single one.  
  - Outperforms all baselines in randomized environments.
- **Adaptive Driving Behavior:**  
  - Maintains higher safety margins in low-friction conditions.  
  - Optimizes efficiency in high-friction environments.  
  - Produces smooth control actions across diverse settings.
- **Distribution Sensitivity:** Policies trained under uniform distributions generalize better to extreme conditions, while LSTM-based models outperform MLP-based policies due to stronger temporal reasoning.

## Outcome
This project demonstrates a unified, memory-aware RL framework capable of **inferring latent environmental variations**, **adapting driving priorities dynamically**, and **maintaining robust performance across diverse and uncertain conditions**. The integration of randomized dynamics, context-aware rewards, and LSTM-based PPO yields significant improvements over domain randomization and environment-specific training.  
The method supports real-time, fine-tuning–free deployment and contributes to ongoing research on robust decision-making and adaptive control in autonomous driving.
