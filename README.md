# Multi-Agent Reinforcement Learning — Delivery Routing

Multi-agent reinforcement learning project using tabular Q-learning for collaborative package delivery routing.

## Overview

This project implements a multi-agent RL system on a 5×5 grid where four agents learn to coordinate
package deliveries between locations A and B. Each agent keeps its own Q-table over the discretized
joint state and learns independently while sharing a common environment clock.

Key features:
- **Tabular Q-Learning** — one Q-table per agent over the joint state (agent positions and delivery phases)
- **Epsilon-Greedy Exploration** — decaying exploration rate for convergence
- **Hybrid Reward Shaping** — movement penalty, stationary penalty, collision penalty, inverse-distance guidance, and delivery bonuses
- **Collision Detection** — penalties when agents in opposite delivery phases meet outside the goal cells
- **Centralized Clock with Simultaneous Learning** — shared environment step counter

## Files

- `Multiagent_RL_Delivery.ipynb` — full project notebook with training, evaluation, and analysis
- `DeepQ_Skeleton.ipynb` — separate exploratory DQN skeleton, not used by the main notebook

## Getting Started

```bash
pip install numpy matplotlib
jupyter notebook Multiagent_RL_Delivery.ipynb
```

## Results

Focal-agent evaluation covers 2 delivery maps × 16 start configurations (all 2⁴ phase assignments).
All four agents reach a 100.00% success rate, where success requires completing the round trip with
zero collisions.
