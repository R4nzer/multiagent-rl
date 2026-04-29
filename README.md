# Multi-Agent Reinforcement Learning — Delivery Routing

Multi-agent reinforcement learning project using Deep Q-Networks for collaborative package delivery routing.

## Overview

This project implements a centralized multi-agent RL system where two agents learn to coordinate package deliveries between locations A and B. The agents use independent Q-learning with centralized training, sharing a common clock and learning simultaneously.

Key features:
- **State Representation** — each agent tracks its own position and package status
- **Epsilon-Greedy Exploration** — decaying exploration rate for convergence
- **Reward Design** — distance guidance, delivery bonuses, collision and stationary penalties
- **Centralized Clock with Simultaneous Learning** — shared environment step counter

## Files

- `Multiagent_RL_Delivery.ipynb` — full project notebook with training, evaluation, and analysis
- `DeepQ_Skeleton.ipynb` — lightweight skeleton for experimentation

## Getting Started

```bash
pip install torch numpy matplotlib
jupyter notebook Multiagent_RL_Delivery.ipynb
```

## Results

The trained agents learn efficient delivery strategies, avoiding collisions and minimizing delivery time through coordinated routing.
